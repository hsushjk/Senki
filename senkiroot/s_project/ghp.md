---
description: S-GHP
---

# Senki-GitHub Proxy

对GitHub Releases , archive , gist , raw.githubusercontent.com 文件代理加速下载服务，无需登录。

## 参数：

* 节点：Cloudflare Workers
* 日请求限制：100000

## 进入：

{% embed url="https://github.senki.top/" %}
S-GHP/
{% endembed %}

## 使用：

#### 在原下载地址前附加S-GHP/的地址：

例子：<mark style="background-color:blue;">https://github.senki.top/</mark><mark style="background-color:purple;">https://github.com/hsushjk/larage-example/releases/download/faketag/example.large</mark>

#### 在S-GHP/界面下载：

在S-GHP/界面的输入框输入符合规范的GitHub链接，然后点击Download按钮

#### 在终端/命令行下载：

支持被 git clone , wget , curl 等工具调用

例子：git clone <mark style="background-color:blue;">https://github.senki.top/</mark><mark style="background-color:purple;">https://github.com/hsushjk/larage-example/releases/download/faketag/example.large</mark>
