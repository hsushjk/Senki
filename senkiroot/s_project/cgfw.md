---
description: C-GFW
---

# Counter GFW

该服务旨在绕过GFW，无视大陆网络审查，使大陆用户能够访问被GFW屏蔽的内容。

{% hint style="info" %}
注意：任何地区的互联网环境都是受到管制的，无一例外，互联网并非法外之地，社长非常不希望用户使用互联网做出损人利己甚至损人不利己的事情。
{% endhint %}

{% hint style="info" %}
声明：千木社对大陆审查制度保持中立态度，拒绝评价。
{% endhint %}

## 内容：

千木社开放了一个香港节点供用户使用：

<pre><code>#位置：香港[Hong Kong]
#速率：30Mbps
#去程线路：
 联通：联通169网络(AS4837) -> 联通169网络(AS4837)，直连网络
<strong> 移动：移动骨干网(AS9808) -> 移动CMI境外骨干网(AS58453)，直连网络
</strong> 电信：电信163骨干网(AS4134) -> CN2(AS4134)，CN2-GT网络
#回程线路：
 联通：联通169网络(AS4837) -> 联通169网络(AS4837)，直连网络
 移动：移动CMI境外骨干网(AS58453) -> 移动骨干网(AS9808)，直连网络
 *有说法是移动回程也是AS4837
 电信：联通169网络(AS4837) -> 联通169网络(AS4837)，直连网络
#月共享流量：1TB
#核心：xray/v2ray
#链接/订阅方式：一次性直链，V2，一次性Base64，Base64
#配置文件：双栈，纯IPv4，纯IPv6，防DNS污染
</code></pre>

## 特点：

1. 隐私防泄漏，千木社以安全为第一位，拒绝监守自盗。
2. 纯净IP，被各大厂商风控警告的可能性小。
3. 兼容IPv6，双栈网络兼容性强。
4. 在线人数少，几乎不用太担心有素质差的邻居。
5. IP固定，免去异地登录带来的封号风险。

## 规则：

1. 请遵守千木社用户规范。
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

针对高级用户：

* 千木社额外提供了<mark style="background-color:blue;">一次性直链，V2，一次性Base64，Base64</mark>订阅方式，根据具体需求进行相应操作即可（Clash链现已停止支持）

#### 3. 进阶设置之打开IPv6

要使用千木社的IPv6，请：

1. 将v2rayNG保持<mark style="color:blue;">关闭连接</mark>状态
2. 单击<mark style="background-color:blue;">左上角</mark>的 <mark style="background-color:blue;">"三"</mark>
3. 单击 <mark style="background-color:blue;">"设置"</mark>
4. 在页面中找到 <mark style="background-color:blue;">"IPv6优先"</mark>
5. 勾选上
6. 回到主页面
7. 现在你可以继续使用了

\*打开IPv6后网速变慢/变卡？请参阅 ["双栈网络兼容"](../v4v6.md)

针对高级用户：

* 当<mark style="background-color:blue;">"IPv6优先"</mark>被<mark style="background-color:red;">打开</mark>时，尽管你只有IPv4你也能访问IPv6资源；反过来说仅有IPv6也能通过C-GFW访问IPv4资源（但此时不勾选<mark style="background-color:blue;">"IPv6优先"</mark>可能会造成代理后的IPv6工作不正常）

#### 4. 进阶设置之选择配置文件

一般情况下，用户只需：

1. 将v2rayNG保持<mark style="color:blue;">关闭连接</mark>状态
2. 单击右上角的 <mark style="background-color:blue;">"三个点"</mark> 样的图标
3. 然后单击 <mark style="background-color:blue;">"测试全部配置真连接"</mark>
4. 等待大约十秒，你会发现<mark style="background-color:blue;">每张配置卡片右上角会有以ms为单位的数字</mark>
5. 选<mark style="background-color:blue;">最低的</mark>那个（<mark style="background-color:red;">-1ms除外</mark>）
6. 不放心的话，你可以多重复几次第 3. 步
7. 现在你可以继续使用了

针对高级用户：

* 配置文件中的 "双栈" "纯IPv4" "纯IPv6" "防DNS污染" 并<mark style="background-color:blue;">不是指连接后你的网络体验会怎么样</mark>，而是<mark style="background-color:blue;">指你的机器将以什么形式与千木社的C-GFW业务进行连接</mark>。用户可根据实际情况进行选择。

### 电脑端(Windows)：

休息休息再写
