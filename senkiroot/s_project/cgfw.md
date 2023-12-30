---
description: C-GFW
---

# Counter GFW

该服务旨在绕过GFW，无视大陆网络审查，使大陆用户能够访问被GFW屏蔽的内容。

{% hint style="info" %}
2023/12/30，社长将cgfw停止公开，此后用户需要主动申请才能使用。
{% endhint %}

{% hint style="info" %}
叠甲：

注意：任何地区的互联网环境都是受到管制的，无一例外，互联网并非法外之地，社长非常不希望用户使用互联网做出损人利己甚至损人不利己的事情

声明：千木社对大陆审查制度保持中立态度，拒绝评价。
{% endhint %}

{% hint style="info" %}
稳定性：

受网络高峰期影响，本节点可能会在某些时间变得比较卡顿，感谢理解

受大陆反制措施影响，节点与用户之间的连接可能会被不定时阻断/Qos/污染/甚至是封锁。这属于不可控因素，具体看地区和特殊时间段。
{% endhint %}

## 内容：

千木社开放了一个香港节点供用户使用：

```
#位置：香港[Hong Kong]
#速率：30Mbps
#去程线路：
 联通：联通169网络(AS4837) -> 联通169网络(AS4837)，直连网络
 移动：移动骨干网(AS9808) -> 移动CMI境外骨干网(AS58453)，直连网络
 电信：电信163骨干网(AS4134) -> CN2(AS4134)，CN2-GT网络
#回程线路：
 联通：联通169网络(AS4837) -> 联通169网络(AS4837)，直连网络
 移动：移动CMI境外骨干网(AS58453) -> 移动骨干网(AS9808)，直连网络
 *有说法是移动回程也是AS4837
 电信：联通169网络(AS4837) -> 联通169网络(AS4837)，直连网络
#月共享流量：1TB
#核心：xray
#链接/订阅方式：请自行向社长申请
#配置文件：网域，IPv4
```

## 特点：

1. 隐私防泄漏，千木社以安全为第一位，拒绝监守自盗。
2. 纯净IP，被各大厂商风控警告的可能性小。
3. 在线人数少，几乎不用太担心有素质差的邻居。
4. IP固定，免去异地登录带来的封号风险。

## 规则：

1. 请参考并遵守千木社用户规范。
2. 尽量不要用于<mark style="background-color:orange;">注册</mark>高度敏感的网站，例如Google（但<mark style="background-color:orange;">登录</mark>可以。

## 连接：

若您为老访客：请通过“S-QS/CGFW”按照提示获得支持

{% embed url="https://sqs.senki.top/cgfw/" %}
S-QS/CGFW
{% endembed %}

若您为新访客：请先查看**使用教程**

## 使用教程：

[单击此文字以快捷跳转至 "电脑端(Windows)："](cgfw.md#dian-nao-duan-windows)

### 手机端v2ray(Android)：

#### 1. 初步设置：

\*\*\*若您使用过v2ray系列客户端且已经<mark style="background-color:blue;">会导入订阅</mark>/<mark style="background-color:blue;">调整域名策略</mark>，您可以跳过这一步，并直接通过“S-QS/CGFW”按照提示获得支持

{% embed url="https://sqs.senki.top/cgfw/" %}
S-QS/CGFW
{% endembed %}

按照视频教程操作即可，其中<mark style="background-color:blue;">视频开头打开的应用是一种浏览器</mark>，<mark style="background-color:blue;">用户自己操作的话用什么浏览器都行，</mark>输入的<mark style="color:blue;">网址为senki.top</mark>，该网址就是千木社官网

{% file src="../../.gitbook/assets/v2rayng.mp4" %}
安卓端(Android)视频教程
{% endfile %}

当你按照视频中进行设置后，<mark style="color:blue;">就已经完成了初始化设置</mark>。

以后<mark style="background-color:blue;">想用就在</mark><mark style="color:red;background-color:blue;">主页面</mark><mark style="background-color:blue;">单击右下角的灰色的"V"图标</mark>，不想用就再点一下即可<mark style="background-color:blue;">关闭连接</mark>。

#### 2 . 进阶设置之主动 <mark style="background-color:blue;">"更新订阅"</mark>

一般情况下，客户端会定期自动更新。但如果没有自动更新，用户只需：

1. 将v2rayNG保持<mark style="color:blue;">关闭连接</mark>状态
2. 单击右上角的 <mark style="background-color:blue;">"三个点"</mark> 样的图标
3. 然后单击 <mark style="background-color:blue;">"更新订阅"</mark>
4. 等待大约不到十秒，知道<mark style="background-color:blue;">弹出 "成功" 的提示</mark>字样
5. 现在你可以继续使用了

### 电脑端(Windows)：

#### 1. 初步设置：

\*\*\*若您使用过v2ray系列客户端且已经<mark style="background-color:blue;">会导入订阅</mark>/<mark style="background-color:blue;">调整域名策略</mark>，您可以跳过这一步，并直接通过“S-QS/CGFW”按照提示获得支持

{% embed url="https://sqs.senki.top/cgfw/" %}
S-QS/CGFW
{% endembed %}

一般情况下，没有v2rayN的用户只需下载千木社整合包：

1. 打开上方的 "S-QS/CGFW" 链接
2. 单击 "适用于Windows的客户端(整合包)" 的 "获取" 链接，并开始下载
3. 打开压缩包，将文件夹 "v2rayN-With-Senki-GFW" 拷贝到一个合适的位置
4. 打开文件夹中的"v2rayN.exe"
5. 程序打开后会自动最小化，这是正常现象。
6. 状态栏<mark style="background-color:blue;">右键单击</mark>图标，选择 <mark style="background-color:blue;">"自动配置系统代理"</mark>
7. 此时已配置完毕并接入节点。若要断开连接退出，请在状态栏<mark style="background-color:blue;">右键单击</mark>图标，选择 <mark style="color:blue;">"清除系统代理"</mark>，即可安全退出！！！若要断开连接退出，请在状态栏<mark style="background-color:blue;">右键单击</mark>图标，选择 <mark style="color:blue;">"清除系统代理"</mark>，即可安全退出！！！

针对高级用户：

* 整合包阉割了一部分核心，导致可能不能兼容其它节点，去GitHub补齐即可

#### 2 . 进阶设置之主动 <mark style="background-color:blue;">"更新订阅"</mark>

一般情况下，客户端会定期自动更新。但如果没有自动更新，用户只需：

1. 将v2rayN保持<mark style="color:blue;">"清除系统代理"</mark>状态
2. 状态栏<mark style="background-color:blue;">右键单击</mark>图标，选择 <mark style="background-color:blue;">"更新全部订阅(不通过代理)"</mark>
3. 等待最多不到十秒，一般即可更新成功（针对更进阶用户：若不放心，可以单击图标打开主界面，查看下方信息日志提示）
4. 现在你可以继续使用了

### 其它操作系统：

：）
