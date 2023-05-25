# 设计目标

### 设计目标 <a href="#she-ji-mu-biao" id="she-ji-mu-biao"></a>

* Xray 内核提供了一个平台，支持必要的网络代理功能，在其之上可以进二次开发，以提供更好的用户体验；
* 以跨平台为首要原则，以减少二次开发的成本；

### 架构 <a href="#jia-gou" id="jia-gou"></a>

![Architecture](broken-reference)

内核分为三层：应用层、代理层和传输层。

每一层内包含数个模块，模块间互相独立，同类型的模块可无缝替换。

#### 应用层 <a href="#ying-yong-ceng" id="ying-yong-ceng"></a>

应用层包含一些代理层中常用的功能，这些功能被抽象出来，以便在不同的代理模块中复用。

应用层的模块应为纯软件实现，与硬件或平台相关的技术无关。

重要模块列表：

* Dispatcher: 用于把入站代理所接收到的数据，传送给出站代理；
* Router: 路由模块，详见 路由配置；
* DNS: 内置的 DNS 服务器模块；
* Proxy Manager: 代理管理器；

#### 代理层 <a href="#dai-li-ceng" id="dai-li-ceng"></a>

代理层分为两部分：入站代理（Inbound Proxy）和出站代理（Outbound Proxy）。

两部分相互独立，入站代理不依赖于某个特定的出站代理，反之亦然。

**入站代理**

* 实现 [proxy.Inboundopen in new window](https://github.com/xtls/Xray-core/blob/main/proxy/proxy.go) 接口；

**出站代理**

* 实现 [proxy.Outboundopen in new window](https://github.com/xtls/Xray-core/blob/main/proxy/proxy.go) 接口；

#### 传输层 <a href="#chuan-shu-ceng" id="chuan-shu-ceng"></a>

传输层提供一些网络数据传输相关的工具模块。
