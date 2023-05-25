# 配置运行

### 配置运行 <a href="#pei-zhi-yun-hang" id="pei-zhi-yun-hang"></a>

[下载并安装](.gitbook/assets/install) 了 Xray 之后，您需要对它进行一下配置。

为了演示，这里只介绍简单的配置方式。更多的模板: [Xray-examplesopen in new window](https://github.com/XTLS/Xray-examples)

如需配置更复杂的功能，请参考更详细的 [配置文件](broken-reference) 中相关说明。

### 服务端配置 <a href="#fu-wu-duan-pei-zhi" id="fu-wu-duan-pei-zhi"></a>

你需要一台防火墙外的服务器，来运行服务器端的 Xray。配置如下：

```
{
  "inbounds": [
    {
      "port": 10086, // 服务器监听端口
      "protocol": "vmess",
      "settings": {
        "clients": [
          {
            "id": "b831381d-6324-4d53-ad4f-8cda48b30811"
          }
        ]
      }
    }
  ],
  "outbounds": [
    {
      "protocol": "freedom"
    }
  ]
}
```

1\
2\
3\
4\
5\
6\
7\
8\
9\
10\
11\
12\
13\
14\
15\
16\
17\
18\
19\
20\


服务器的配置中需要确保 `id` 和端口与客户端一致，就可以正常连接了。

### 客户端配置 <a href="#ke-hu-duan-pei-zhi" id="ke-hu-duan-pei-zhi"></a>

在你的 PC（或手机）中，需要用以下配置运行 Xray ：

```
{
  "inbounds": [
    {
      "port": 1080, // SOCKS 代理端口，在浏览器中需配置代理并指向这个端口
      "listen": "127.0.0.1",
      "protocol": "socks",
      "settings": {
        "udp": true
      }
    }
  ],
  "outbounds": [
    {
      "protocol": "vmess",
      "settings": {
        "vnext": [
          {
            "address": "server", // 服务器地址，请修改为你自己的服务器 ip 或域名
            "port": 10086, // 服务器端口
            "users": [
              {
                "id": "b831381d-6324-4d53-ad4f-8cda48b30811"
              }
            ]
          }
        ]
      }
    },
    {
      "protocol": "freedom",
      "tag": "direct"
    }
  ],
  "routing": {
    "domainStrategy": "IPOnDemand",
    "rules": [
      {
        "type": "field",
        "ip": ["geoip:private"],
        "outboundTag": "direct"
      }
    ]
  }
}
```

1\
2\
3\
4\
5\
6\
7\
8\
9\
10\
11\
12\
13\
14\
15\
16\
17\
18\
19\
20\
21\
22\
23\
24\
25\
26\
27\
28\
29\
30\
31\
32\
33\
34\
35\
36\
37\
38\
39\
40\
41\
42\
43\
44\


上述配置唯一要更改的地方是你的服务器 IP，配置中已注明。上述配置会把除局域网（比如访问路由器）以外的所有流量转发至你的服务器。

### 运行 <a href="#yun-hang" id="yun-hang"></a>

* 在 Windows 和 macOS 中，配置文件通常是 Xray 同目录下的 `config.json` 文件。
  * 直接运行 `Xray` 或 `Xray.exe` 即可。
* 在 Linux 中，配置文件通常位于 `/etc/xray/` 或 `/usr/local/etc/xray/` 目录下。
  * 运行 `xray run -c /etc/xray/config.json`
  * 或使用 systemd 等工具将 Xray 作为服务在后台运行。

更多详细的说明可以参考 [配置文档](broken-reference) 和 [小小白话文](broken-reference)。
