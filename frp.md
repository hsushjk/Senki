# Senki-FRP

> 这个章节将展示“Senki-FRP”的有关信息

{% hint style="info" %}
该服务并不能助你突破网络封锁，但确实可以让Web服务免备案。
{% endhint %}

## 描述：

FRP 是一个专注于内网穿透的高性能的反向代理应用，支持 TCP、UDP、HTTP、HTTPS 等多种协议。可以将内网服务以安全、便捷的方式通过具有公网 IP 节点的中转暴露到公网。

## 特点：

* 轻松地将内网服务穿透到公网。
* 客户端服务端通信支持 TCP、KCP 以及 Websocket 等多种协议。
* 采用 TCP 连接流式复用，在单个连接间承载更多请求，节省连接建立时间。
* 代理组间的负载均衡。
* 端口复用，多个服务通过同一个服务端端口暴露。
* 多个原生支持的客户端插件（静态文件查看，HTTP、SOCK5 代理等），便于独立使用 frp 客户端完成某些工作。
* 高度扩展性的服务端插件系统，方便结合自身需求进行功能扩展。
* 服务端和客户端 UI 页面。

## [ ](https://gofrp.org/docs/overview/#%E4%B8%8B%E4%B8%80%E6%AD%A5)Senki-FRP专有特点：

* 低延迟，(游戏)延迟最低可以达到90ms（测试环境：电信网络，Minecraft服务器）
* 免费，无需注册任何账号
* 纯净，大陆审查不会将此判断为诈骗站点/ip
* 带宽亲人，提供最大30Mbps的带宽

## 规则：

* 禁止用于反政府/儿童色情/性虐待/走私枪支弹药/毒品/诈骗

## 参数：

请进入QS界面查看

{% embed url="https://frp.senki.top/" %}
Senki-FRP
{% endembed %}

## 使用：

### 针对小白用户：

#### Windows 端：

1. 转到快速支持页或者直接单击下方按钮，选择 “Windows客户端” 下载

{% embed url="https://frp.senki.top/" %}
Senki-FRP
{% endembed %}

2. 将文件解压，参照 “配置示例.ini” 来修改配置，将修改好的配置粘贴在“frpc.ini"并保存
3. 启动 “Senki-FRP客户端.bat” 观察运行是否正常

#### Android 端：

{% hint style="info" %}
兼容性可能较差，原作者上一次更新还是在2022中旬
{% endhint %}

1. 转到快速支持页或者直接单击下方按钮，选择 “Android客户端” 下载

{% embed url="https://frp.senki.top/" %}
Senki-FRP
{% endembed %}

2. 继续在刚刚的页面单击 “基础配置文件：frpc.ini 获取”
3. 选择FRPC，单击右上角铅笔图案，删除所有内容，将获取到的 “frpc.ini” 中的内容复制到其中
4. 将 “#示例内容” 以下的参数按照你的需求进行更改，保存
5. 按右下角图标开启，观察运行是否正常

#### 其它操作系统：

\#请问你真的是小白吗

### 针对高级用户：

\#高级用户不需要我教