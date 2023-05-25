# 编译文档

### 编译文档 <a href="#bian-yi-wen-dang" id="bian-yi-wen-dang"></a>

### 前序工作 <a href="#qian-xu-gong-zuo" id="qian-xu-gong-zuo"></a>

Xray 使用 [Golangopen in new window](https://golang.org/) 作为编程语言，你需要先安装最新版本 Golang 才能够编译。

> 如果你不幸使用 Windows, 请 **务必** 使用 Powershell

### 拉取 Xray 源代码 <a href="#la-qu-xray-yuan-dai-ma" id="la-qu-xray-yuan-dai-ma"></a>

```
git clone https://github.com/XTLS/Xray-core.git
cd Xray-core && go mod download
```

1\
2\


> 如果你闲的没事干，可以试试 GitHub 官方工具: `gh repo clone XTLS/Xray-core`

注意：在无法正常访问 Google 的网络环境，依赖无法被正常拉取，需要先设置 `GOPROXY`：

```
go env -w GOPROXY=https://goproxy.io,direct
```

1\


### 构建二进制 <a href="#gou-jian-er-jin-zhi" id="gou-jian-er-jin-zhi"></a>

#### Windows(Powershell): <a href="#windows-powershell" id="windows-powershell"></a>

```
$env:CGO_ENABLED=0
go build -o xray.exe -trimpath -ldflags "-s -w -buildid=" ./main
```

1\
2\


#### macOS, Linux: <a href="#macos-linux" id="macos-linux"></a>

```
CGO_ENABLED=0 go build -o xray -trimpath -ldflags "-s -w -buildid=" ./main
```

1\


运行以上命令会在目录下生成 xray 可执行文件。

提示

如果需要编译可以进行 debug 的程序,即可以用 dlv 附加到运行的程序进行调试, 请去掉 ldflags 中的 '-w -s' 选项.

\-w 禁止生成 debug 信息。使用该选项后，将无法使用 gdb 进行调试。 -s 禁用符号表 PS:其实用 vscode 或其他 IDE 调试似乎更方便。

### 交叉编译： <a href="#jiao-cha-bian-yi" id="jiao-cha-bian-yi"></a>

这里以在 Windows(Powershell) 环境中，编译到 Linux 服务器为例：

```
$env:CGO_ENABLED=0
$env:GOOS="linux"
$env:GOARCH="amd64"

go build -o xray -trimpath -ldflags "-s -w -buildid=" ./main
```

1\
2\
3\
4\
5\


上传到服务器后，记得在服务器终端内执行 `chmod +x xray`

提示

执行 `go tool dist list` 查看所有支持的系统与架构。

### 可复现构建： <a href="#ke-fu-xian-gou-jian" id="ke-fu-xian-gou-jian"></a>

按照上述步骤，能够编译与 Release 中完全相同的二进制文件。

注意

请先确认您使用的 Golang 版本与编译 Release 的一致。
