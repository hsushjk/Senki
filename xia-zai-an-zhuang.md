# 下载安装

### 下载安装 <a href="#xia-zai-an-zhuang" id="xia-zai-an-zhuang"></a>

### 平台支持 <a href="#ping-tai-zhi-chi" id="ping-tai-zhi-chi"></a>

Xray 在以下平台中可用：

* Windows 7 及之后版本（x86 / amd64 / arm32 / arm64）；
* macOS 10.10 Yosemite 及之后版本（amd64 / arm64）；
* Linux 2.6.23 及之后版本（x86 / amd64 / arm / arm64 / mips64 / mips / ppc64 / s390x / riscv64）；
  * 包括但不限于 Debian 7 / 8、Ubuntu 12.04 / 14.04 及后续版本、CentOS 7 / 8、Arch Linux 等；
* FreeBSD (x86 / amd64)；
* OpenBSD (x86 / amd64)；
* Dragonfly BSD (amd64)；

### 下载 Xray <a href="#xia-zai-xray" id="xia-zai-xray"></a>

预编译的二进制 ZIP 格式压缩包可在 [Github Releasesopen in new window](https://github.com/xtls/Xray-core/releases) 中找到。

下载对应平台的压缩包，解压后即可使用。

### 验证安装包 <a href="#yan-zheng-an-zhuang-bao" id="yan-zheng-an-zhuang-bao"></a>

Xray 提供两种验证方式：

* ZIP 压缩包的 SHA1 / SHA256 摘要
* 可复现构建：请参照 [编译 Xray](broken-reference)

### Windows 安装方式 <a href="#windows-an-zhuang-fang-shi" id="windows-an-zhuang-fang-shi"></a>

* 在 [Github Releasesopen in new window](https://github.com/xtls/Xray-core/releases) 下载适用于 Windows 平台的 ZIP 压缩包，解压后可得到可执行文件 `xray.exe` ，然后[通过命令行带参数运行](.gitbook/assets/command) 即可
* 通过 [Scoopopen in new window](https://scoop.sh/) 包管理器安装：Xray 已经被添加到 [Mochiopen in new window](https://github.com/Qv2ray/mochi)。

### macOS 安装方式 <a href="#macos-an-zhuang-fang-shi" id="macos-an-zhuang-fang-shi"></a>

* 在 [Github Releasesopen in new window](https://github.com/xtls/Xray-core/releases) 下载适用于 macOS 平台的 ZIP 压缩包，解压后可得到可执行文件 `xray` ，然后[通过命令行带参数运行](broken-reference) 即可
* 通过 [Homebrewopen in new window](https://brew.sh/) 包管理器安装：`brew install xray`
* [homebrew-xrayopen in new window](https://github.com/N4FA/homebrew-xray) 感谢[@N4FAopen in new window](https://github.com/N4FA)

### Linux 安装方式 <a href="#linux-an-zhuang-fang-shi" id="linux-an-zhuang-fang-shi"></a>

#### 安装脚本 <a href="#an-zhuang-jiao-ben" id="an-zhuang-jiao-ben"></a>

* Linux Script
  * [Xray-installopen in new window](https://github.com/XTLS/Xray-install)
* One Click
  * [Xray-scriptopen in new window](https://github.com/kirin10000/Xray-script)
  * [ProxySUopen in new window](https://github.com/proxysu/ProxySU)
  * [v2ray-agentopen in new window](https://github.com/reeceyng/v2ray-agent) 感谢[@mack-aopen in new window](https://github.com/mack-a) [@Reeceopen in new window](https://github.com/reeceyng)
  * [Xray-yesopen in new window](https://github.com/jiuqi9997/Xray-yes)
  * [Xray-onekeyopen in new window](https://github.com/wulabing/Xray\_onekey)
* Magisk
  * [Xray4Magiskopen in new window](https://github.com/CerteKim/Xray4Magisk)
  * [Xray\_For\_Magiskopen in new window](https://github.com/E7KMbb/Xray\_For\_Magisk)

#### Arch Linux <a href="#arch-linux" id="arch-linux"></a>

**Arch User Repository**

需要使用 [AUR helpersopen in new window](https://wiki.archlinux.org/index.php/AUR\_helpers)，以 [yayopen in new window](https://github.com/Jguer/yay) 为例，可通过 `yay -S xray` 安装。

**Arch Linux CN**

首先添加 [Arch Linux CN 仓库open in new window](https://www.archlinuxcn.org/archlinux-cn-repo-and-mirror/)，然后在 root 用户下使用 `pacman -S xray` 安装。

#### Linuxbrew <a href="#linuxbrew" id="linuxbrew"></a>

Linuxbrew 包管理器的使用方式与 Homebrew 一致：`brew install xray`

#### Debian WIP <a href="#debian" id="debian"></a>

#### Gentoo <a href="#gentoo" id="gentoo"></a>

目前有三个第三方 Overlay 提供 Portage 安装脚本:

* [CHN-beta/touchfish-osopen in new window](https://github.com/gentoo-mirror/touchfish-os/tree/master/net-proxy/Xray): 个人维护，适用于 systemD 系统
* [Gentoo-zhopen in new window](https://github.com/microcai/gentoo-zh): 社区维护，适用于 systemD 系统
* [JuanCldCmt/Xray-Overlayopen in new window](https://github.com/JuanCldCmt/Xray-Overlay)：个人维护，适用于 openRC 系统，同时使用 xray 用户组运行以提高安全性

使用 layman 或 eselect-repository 添加 Overlay 至本地，然后即可安装。

### Docker 安装方式 <a href="#docker-an-zhuang-fang-shi" id="docker-an-zhuang-fang-shi"></a>

* [teddysun/xrayopen in new window](https://hub.docker.com/r/teddysun/xray)

#### Docker image 的文件结构 <a href="#dockerimage-de-wen-jian-jie-gou" id="dockerimage-de-wen-jian-jie-gou"></a>

* `/etc/xray/config.json`：配置文件
* `/usr/bin/xray`：Xray 主程序
* `/usr/local/share/xray/geoip.dat`：IP 数据文件
* `/usr/local/share/xray/geosite.dat`：域名数据文件

### 图形化客户端 <a href="#tu-xing-hua-ke-hu-duan" id="tu-xing-hua-ke-hu-duan"></a>

* OpenWrt
  * [PassWallopen in new window](https://github.com/xiaorouji/openwrt-passwall)
  * [Hello Worldopen in new window](https://github.com/jerrykuku/luci-app-vssr)
  * [ShadowSocksR Plus+open in new window](https://github.com/fw876/helloworld)
  * [luci-app-xrayopen in new window](https://github.com/yichya/luci-app-xray) ([openwrt-xrayopen in new window](https://github.com/yichya/openwrt-xray))
* Windows
  * [v2rayNopen in new window](https://github.com/2dust/v2rayN)
  * [Qv2rayopen in new window](https://github.com/Qv2ray/Qv2ray) （该项目已冻结存档）
  * [Netch (NetFilter & TUN/TAP)open in new window](https://github.com/NetchX/Netch) （该项目已冻结存档）
* Android
  * [v2rayNGopen in new window](https://github.com/2dust/v2rayNG)
  * [Kitsunebiopen in new window](https://github.com/rurirei/Kitsunebi/tree/release\_xtls)
* iOS / macOS（使用 ARM 芯片）
  * [Shadowrocketopen in new window](https://apps.apple.com/app/shadowrocket/id932747118)
  * [Stashopen in new window](https://apps.apple.com/app/stash/id1596063349)
* macOS（X86 芯片 / ARM 芯片）
  * [Qv2rayopen in new window](https://github.com/Qv2ray/Qv2ray) （该项目已冻结存档）
  * [V2RayXSopen in new window](https://github.com/tzmax/V2RayXS)

### UUID 生成器 <a href="#uuid-sheng-cheng-qi" id="uuid-sheng-cheng-qi"></a>

第三方的 UUID 生成器 [uuidgenerator.netopen in new window](https://www.uuidgenerator.net/)
