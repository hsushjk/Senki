# mKCP 协议

mKCP 是流式传输协议，由 [KCP 协议open in new window](https://github.com/skywind3000/kcp) 修改而来，可以按顺序传输任意的数据流。

### 版本 <a href="#ban-ben" id="ban-ben"></a>

mKCP 没有版本号，不保证版本之间兼容性。

### 依赖 <a href="#yi-lai" id="yi-lai"></a>

#### 底层协议 <a href="#di-ceng-xie-yi" id="di-ceng-xie-yi"></a>

mKCP 是一个基于 UDP 的协议，所有通讯使用 UDP 传输。

#### 函数 <a href="#han-shu" id="han-shu"></a>

* fnv: [FNV-1aopen in new window](https://en.wikipedia.org/wiki/Fowler%E2%80%93Noll%E2%80%93Vo\_hash\_function) 哈希函数
  * 输入参数为任意长度的字符串；
  * 输入出一个 32 位无符号整数；

### 通讯过程 <a href="#tong-xun-guo-cheng" id="tong-xun-guo-cheng"></a>

1. mKCP 将数据流拆成若干个数据包进行发送。一个数据流有一个唯一标识，用以区分不同的数据流。数据流中的每一个数据包都携带了同样的标识。
2. mKCP 没有握手过程，当收到一个数据包时，根据其携带的数据流的标识来判断是否为新的通话，或是正在进行中的通话。
3. 每一个数据包中包含若干个片段（Segment），片段分为三类：数据（Data）、确认（ACK）、心跳（Ping）。每个片段需要单独处理。

### 数据格式 <a href="#shu-ju-ge-shi" id="shu-ju-ge-shi"></a>

#### 数据包 <a href="#shu-ju-bao" id="shu-ju-bao"></a>

| 4 字节   | 2 字节   | L 字节 |
| ------ | ------ | ---- |
| 认证信息 A | 数据长度 L | 片段部分 |

其中：

* 认证信息 A = fnv(片段部分），big endian；
* 片段部分可能包含多个片段；

#### 数据片段 <a href="#shu-ju-pian-duan" id="shu-ju-pian-duan"></a>

| 2 字节    | 1 字节   | 1 字节   | 4 字节   | 4 字节   | 4 字节       | 2 字节   | Len 字节 |
| ------- | ------ | ------ | ------ | ------ | ---------- | ------ | ------ |
| 标识 Conv | 指令 Cmd | 选项 Opt | 时间戳 Ts | 序列号 Sn | 未确认序列号 Una | 长度 Len | 数据     |

其中：

* 标识 Conv: mKCP 数据流的标识
* 指令 Cmd: 常量 0x01
* 选项 Opt: 可选的值有：
  * 0x00: 空选项
  * 0x01: 对方已发出所有数据
* 时间戳 Ts: 当前片段从远端发送出来时的时间，big endian
* 序列号 Sn: 该数据片段时数据流中的位置，起始片段的序列号为 0，之后每个新片段按顺序加 1
* 未确认序列号 Una: 远端主机正在发送的，且尚未收到确认的最小的 Sn

#### 确认片段 <a href="#que-ren-pian-duan" id="que-ren-pian-duan"></a>

| 2 字节    | 1 字节   | 1 字节   | 4 字节   | 4 字节       | 4 字节   | 2 字节   | Len \* 4 字节 |
| ------- | ------ | ------ | ------ | ---------- | ------ | ------ | ----------- |
| 标识 Conv | 指令 Cmd | 选项 Opt | 窗口 Wnd | 下一接收序列号 Sn | 时间戳 Ts | 长度 Len | 已收到的序列号     |

其中：

* 标识 Conv: mKCP 数据流的标识
* 指令 Cmd: 常量 0x00
* 选项 Opt: 同上
* 窗口 Wnd: 远端主机可以接收的最大序列号
* 下一接收序列号 Sn: 远端主机未收到的数据片段中的最小序列号
* 时间戳 Ts: 远端主机最新收到的数据片段的时间戳，可用于计算延迟
* 已收到的序列号: 每个 4 字节，表示此序列号的数据已经确认收到

注释：

* 远程主机期待收到序列号 \[Sn, Wnd) 范围内的数据

#### 心跳片段 <a href="#xin-tiao-pian-duan" id="xin-tiao-pian-duan"></a>

| 2 字节    | 1 字节   | 1 字节   | 4 字节       | 4 字节       | 4 字节   |
| ------- | ------ | ------ | ---------- | ---------- | ------ |
| 标识 Conv | 指令 Cmd | 选项 Opt | 未确认序列号 Una | 下一接收序列号 Sn | 延迟 Rto |

其中：

* 标识 Conv: mKCP 数据流的标识
* 指令 Cmd: 可选的值有
  * 0x02: 远端主机强行终止会话
  * 0x03: 正常心跳
* 选项 Opt: 同上
* 未确认序列号 Una: 同数据片段的 Una
* 下一接收序列号 Sn: 同确认片段的 Sn
* 延迟 Rto: 远端主机自己计算出的延迟
