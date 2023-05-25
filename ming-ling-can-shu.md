# 命令参数

### 命令参数 <a href="#ming-ling-can-shu" id="ming-ling-can-shu"></a>

### 获取基本命令 <a href="#huo-qu-ji-ben-ming-ling" id="huo-qu-ji-ben-ming-ling"></a>

您可以运行 `xray help` 来获得所有 xray 最基础的用法, 以及可用的命令及说明.

```
Xray is a platform for building proxies.

Usage:

        xray <command> [arguments]

The commands are:

        run          Run Xray with config, the default command
        version      Show current version of Xray
        api          Call an API in an Xray process
        tls          TLS tools
        uuid         Generate new UUIDs

Use "xray help <command>" for more information about a command.
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


#### xray run <a href="#xray-run" id="xray-run"></a>

指定一个或多个配置文件，并运行。

使用方法:

```
 xray run [-c config.json] [-confdir dir]
```

1\


```
Run Xray with config, the default command.

The -config=file, -c=file flags set the config files for
Xray. Multiple assign is accepted.

The -confdir=dir flag sets a dir with multiple json config

The -format=json flag sets the format of config files.
Default "auto".

The -test flag tells Xray to test config files only,
without launching the server
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


提示

配置文件除了默认的 JSON 格式外，也可以使用 TOML 和 YAML。在不指定格式的前提下会通过文件扩展名识别。

#### xray version <a href="#xray-version" id="xray-version"></a>

输出 Xray 版本、 Golang 版本等信息。

使用方法:

#### xray api <a href="#xray-api" id="xray-api"></a>

调用 Xray 的 gRPC API，需要在配置文件中开启。

使用方法:

```
xray api <command> [arguments]
```

1\


```
        restartlogger Restart the logger
        stats         Get statistics
        statsquery    Query statistics
        statssys      Get system statistics
        adi           Add inbounds
        ado           Add outbounds
        rmi           Remove inbounds
        rmo           Remove outbounds
```

1\
2\
3\
4\
5\
6\
7\
8\


#### xray tls <a href="#xray-tls" id="xray-tls"></a>

一些与 TLS 相关的工具。

使用方法:

```
xray tls <command> [arguments]
```

1\


```
        cert          Generate TLS certificates
        ping          Ping the domain with TLS handshake
        certChainHash Calculate TLS certificates hash.
```

1\
2\
3\


#### xray uuid <a href="#xray-uuid" id="xray-uuid"></a>

生成 UUID。

使用方法:

```
xray uuid [-i "example"]
```

1\


提示

当 `-config` 没有指定时，Xray 将先后尝试从以下路径加载 `config.json` :

* 工作目录（Working Directory）
* 环境变量中 `Xray.location.asset` 所指定的路径
