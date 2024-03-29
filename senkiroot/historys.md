---
description: Senki-Historys
---

# 📜 千木社大事记

### 2024-03-10 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 紧急上线Senki-Kiwix\[千木社无界图书馆]
* 明天过后就忙了，更不可能有精力维护，千木社能活多久取决于我的剩余热情和大家的捐助。
* Milk Cap 365在今年的改革议案中出现分歧，进而有了豁免制度。由于相关工作量太大，本人决定不跟随更新千木社，但本人仍然希望各位用户以客观中立的身份去调用千木社资源。今后出现意外本人很难为你们兜底。

### 2024-02-19 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 结束了为期约4天的热更新，修复了n处暗病，n处bug，重构大量服务，重构大量H5\_UI
* 留出完整的内测通道
* 上线第三方的一个实用demo“94list-demo”
* 千木社注意到新年前后有大量的（无效的）恶意攻击行为。千木社自始至终都在亏钱做免费服务，所以说攻击者就算把千木社成功干倒实际上也和现在也没什么两样，对本人没什么精神和钱财影响。因此请攻击者自重或者找点别的事干干，感谢。

### 2024-02-10 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 2024年新年快乐。新的一年祝大家万事顺遂，健康如意
* 更新了节日祝福元素

### 2024-02-02 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 为禁ping导致KMS激活脚本工作异常做出让步（解除禁ping）

### 2024-01-25 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

新网络接口公测

新网络接口开始公测，地址为hk-net2.senki.top

新接口优点：带宽翻倍\[最高5Gbps，但受限于性能,可能才平均200-300Mbps]，支持IPv6

新接口缺点：延迟变高，丢包率变高

公测结束后，第一接口继续保留，由于新接口存在明显丢包问题，因此依旧为第一接口为主

接口适配范围：全部服务

### 2024-01-24 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 准备添加新的网络接口，因此在公测前，会临时调整原网络接口的策略
* 删除用户自助诊断工具集，单独保留其中的mstest，改为Network-Test，入口位于每个通用网络接口页面的下方

### 2024-01-16 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 限制frp可用于穿透的端口范围，改为理论上10000以上的端口号用户可用。
* 热更新，修复bug，更改规则(frp)
* 热更新，优化用户体验(cgfw)

### 2024-01-14 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 归档完毕
* 虽然在半个月前为了用户体验撤掉了IP封锁，但为了稳定性，千木社稍微增强了防御性保护，可以阻断小规模攻击，拦截部分恶意请求和防止海外势力扫描
* 千木社建议大家使用NekoBox和NekoRay，v2也可，但依旧非常不愿意大家使用Clash系客户端
* 请不要套用第三方代理使用千木社服务，请不要以不正常的方式使用千木社服务，千木社服务暂不对海外用户开放和提供技术支持

### 2024-01-01 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 抢修完毕，ip已更换
* 千木社大维护已结束

### 2023-12-31 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 有反馈称新IP疑似被部分平台屏蔽，且有较大的网络波动。情况属实，将在明年零点后修复

### 2023-12-30 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 千木社进行大维护，将会削减/优化/转换项目与资源：

1. 1.smsg简讯服务优化&#x20;
2. IPv4更换&#x20;
3. IPv6撤除&#x20;
4. 停止恶意IP地址封锁
5. 撤除镜像站
6. 停运warp
7. 停运GitHub加速
8. 重置并隐藏cgfw

### 2023-12-29 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 千木社准备进入归档程序

### 2023-12-12 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 千木社IPv4/6遭到部分平台拉黑（例如谷歌），具体原因为某些用户使用千木社代理网络进行网络爬虫和攻击。

### 2023-11-20 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 千木简讯第一次被正式使用
* 为了保障用户的网络安全，千木社本次向封锁名单中加入5936个恶意IP地址和一个DNS客户，这是首次预防性封锁。IP名单来自“清华大学网络与信息安全实验室”，“FeodoTracker”等国内外具有权威性的安全实验室，包括IPv4和IPv6，并且定期更新。
* 维基媒体系列的镜像站已恢复，详阅 [Wikimedia(维基媒体)](broken-reference)

### 2023-11-18 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 千木社其实是有api的，使用api调取简讯，起初的确想做官方app，但后来觉得也没必要，单纯留着api也没啥用。今天改成千木简讯，官网就是senki.top/smsg，去senki.top就能看到

### 2023-10-15 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* www.senki.top可以使用 普通搜索 + AI解答 ，用户可以在搜索栏直接提问千木社中已有的内容，AI将会把内容整合后作为解答返回给用户。

### &#x20;2023-10-13 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* S\_DMS(千木网域镜像站)已上线，是各个海外网域镜像站的超集。致力于将不易访问的站点以镜像的方式呈现给用户。

### 2023-10-12 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* Counter GFW更新，此次更新终止了对Clash Link/猫猫链的支持。用户可能依旧能够使用已有的配置文件，但将无法得到更新和迁移提示。拓展支持将在下一次优化被取代。
* 为了让用户在使用时出现问题时能够自行诊断，故推出 “S\_USSDT” 。用户可使用该工具集自主判断问题。因为该工具集为调试诊断工具，无需迭代维护和频繁优化，故独立于S\_Project和S-QS
* mstest(延迟测试)已发布，用于测试从用户端到千木社服务器的时延。属于 “S\_USSDT” 的一部分。

### 2023-09-23 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* “电子邮件路由(傀儡邮件地址)”立项中止，方案废除。原因：不符合千木社理念。有这个需求的一般有能力直接注册免费域名自己搭建，更方便管理且更安全。成立该项目只会让使用者事倍功半。
* “二级域名分发系统”立项中止，方案废除。原因：不符合千木社理念。有这个需求的一般有能力直接注册免费域名自己用，更方便管理且更安全。成立该项目只会让使用者事倍功半。
* “Google搜索 镜像站”立项可行。计划将更多实用性和需要随用随开的站点进行镜像。

### 2023-09-18 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* ~~“电子邮件路由(傀儡邮件地址)”立项~~（中止）
* ~~“二级域名分发系统”立项~~（中止）
* “Google搜索 镜像站”立项

### 2023-09-13 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 千木社全站维护完毕
* Senki-Zerotier服务/项目公测未通过。Zerotier主要用udp打洞直连，基本上不怎么用tcp，一般顶多用tcp中转。用udp的后果是被某些地区的运营商疯狂QoS。。。这不是打洞不畅，这是丢包严重，可能连moon中转都触发不了。我不知道为什么那么多up主博主吹这个，又不可控又不加密又是udp-Qos，早在2020年就死球了！这种组VPN的东西及其容易被ISP识别（不管你是不是用来科学上网），几乎从来没有活久的方法，除非你买国内服务。
* Senki-MCJava因为长时间没人玩，服务不活跃，因此停了。但是没移除，改归档状态，留个念想。
* NTP服务器恢复运行

### 2023-09-12 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* Senki-FRP维护完毕
* Senki-FRP虚拟主机穿透关停，什么时候有新机再开，要不然没啥意义
* Senki-FRP服务端版本更新，并将x86/x64/arch64一同合并进windows客户端整合包
* 为几乎所有S-QS界面添加了上次更新时间，该时间通过读取www.senki.top的源markdown文件的修改时间进行同步。

### 2023-09-09 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* Counter GFW（C-GFW）维护完毕
* WARP 维护完毕
* Senki-KMS 维护完毕

### 2023-09-08 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* IPv6地址更换一次，此次更换解除了Google对千木社IPv6的风控
* 对Counter GFW（C-GFW）服务进行大改，去掉了兼容性较差的Clash链。为补偿空缺，在保留"直链"的基础上增加了base64通用链。

### 2023-09-07 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 全站服务开始恢复
* IPv6地址更换一次

### 2023-09-06 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* IPv6与双栈实现方式已敲定并开始部署

### 2023-09-05 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 千木社开始接入双栈网络，全站将额外支持IPv6（特殊情况除外）
* 千木社全站停机，进行了大量优化，部分内容推倒重建

### 2023-08-20 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 修复了KMS服务

### 2023-07-05 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 预上线 MemMgr

### 2023-06-22 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 社长这几天病了，很多事情一直在鸽
* 上线 NTP服务器
* 上线 KMS激活服务器
* 上线 生命周期策略
* 补全前端
* 砍掉 DNS服务，因为稳定性不达标，ip不好记，不支持ipv6，延迟高，没必要存在了。

### 2023-06-18

* GitHub镜像站 疑似被攻击，
* GitHub镜像站 自测存在安全风险，故关停。
* GitHub镜像站 改为 GitHub加速站

### 2023-06-17

* GitHub镜像站 搭建完毕，~~嘎嘎好用~~，还能登录

### 2023-06-06 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 怎么说，祝全中国高考考生金榜题名，超常发挥。衷心希望所有考生不忘带考试用品，每道题都拿手，作答期间不生病，晚上睡觉不失眠。
* 计划在2024年新年当天停运，请查阅 关于停运

### 2023-06-05 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 修缮了一下FRP，顺便把入口和使用手册上线

### 2023-05-26 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 将主页改为在线文档，使用Gitbook搭建，下放到www.
* 已将S\_Project和Milk Cap 365对接

### 2023-05-25 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

* 因为社长的强迫症犯了，千木社开始重建，为了方便管理(方便摸鱼)，社长把所有的已搭建服务和预搭建服务整合在一起，合并为S\_Project，准备和Milk Cap 365对接
* 社长花了两天时间摸透了Cloudflare Warp+，发现确实比较好用\[网上相关资料好少]
* （社长鸽了一晚上）

### And More...... <a href="#id-2020-11-23" id="id-2020-11-23"></a>

鸽，不想写了，这好比学生把假期的作业堆到最后，更不想写了。

### 2022-7-22 <a href="#id-2020-11-23" id="id-2020-11-23"></a>

域名 Senki.top 被社长注册，原先的.tk系域名被弃用，将原先的云存储/网站托管/博客迁移到了Senki.top

> ~~梦开始的时候~~
