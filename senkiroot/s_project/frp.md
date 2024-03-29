---
description: S-FRP
---

# Senki-FRP

FRP 是一个专注于内网穿透的高性能的反向代理应用，支持 TCP、UDP、<mark style="background-color:orange;">HTTP、HTTPS（注：千木社暂不支持穿透http(s)）</mark> 等多种协议。可以将内网服务以安全、便捷的方式通过具有公网 IP 的节点中转暴露到公网。

Senki-FRP是千木社提供的免费FRP服务。

## 大致配置：

\#请参考[Universal Network Interface(通用网络接口)](../uni/)

## 特点：

* 轻松地将内网服务穿透到公网。
* 客户端服务端通信支持 TCP、KCP 以及 Websocket 等多种协议。
* 采用 TCP 连接流式复用，在单个连接间承载更多请求，节省连接建立时间。
* 代理组间的负载均衡。
* 端口复用，多个服务通过同一个服务端端口暴露。
* 高度扩展性的服务端插件系统，方便结合自身需求进行功能扩展。

## [ ](https://gofrp.org/docs/overview/#%E4%B8%8B%E4%B8%80%E6%AD%A5)Senki-FRP专有特点：

* 免费，无需注册任何账号
* 纯净，大陆审查不会将此判断为诈骗站点/ip

## Senki-FRP缺点：

* 无法用于搭建正常的80/443端口网站
* 只有10000以上的端口可用（为了防止冒充而做出的限制，请见谅）

## 规则：

* 请参考并遵守千木社用户规范。

## 快速支持：

{% embed url="https://sqs.senki.top/frp" %}
S-QS/FRP
{% endembed %}

## 使用：

### 针对小白用户：

#### Windows 端：

1. 转到"S-QS/FRP"，选择 “Windows客户端” 下载
2. 将文件解压，参照 “配置示例.ini” 来修改配置，将修改好的配置粘贴在“frpc.ini"并保存
3. 启动 “Senki-FRP客户端.bat” 并观察frpc.log来判断运行是否正常

#### Android 端：

{% hint style="info" %}
兼容性可能较差，原作者上一次更新还是在2022中旬
{% endhint %}

1. 转到"S-QS/FRP"，选择 “Android客户端” 下载
2. 继续在刚刚的页面单击 “基础配置文件：frpc.ini 获取”
3. 选择FRPC，单击右上角铅笔图案，删除所有内容，将获取到的 “frpc.ini” 中的内容复制到其中
4. 将 “#示例内容” 以下的参数按照你的需求进行更改，保存
5. 按右下角图标开启，观察运行是否正常

#### 其它操作系统：

：）

### 针对高级用户：

本FRP服务未魔改，更多功能请自行探索
