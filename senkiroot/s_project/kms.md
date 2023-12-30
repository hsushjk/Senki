---
description: S-KMS
---

# Senki-KMS

KMS是密钥管理服务（Key Management Server），即通过系统管理员（System Administrator）使用一个批量激活密钥（Volume Key），设置一个激活服务器（Activation Server），并在每一个客户机上安装KMS的客户端，就可以进行批量激活和管理，是自从Windows Vista后微软开始使用的一种大型组织中的批量激活技术。

Senki-KMS为千木社自建的KMS激活服务

## 支持范围：

### KMS产品：

MS Office：2010/2013/2016/2019/2021 MS-365

Windows(零售/批量): Vista/7/8/8.1/10/11 LTSB/LTSC 神州网信

Windows(Server): 2008/2008R2/2012/2012R2/2016/2019/2022

### KMS协议：

* Protocol v4
* Protocol v5
* Protocol v6

## 参数：

* 请访问快速支持

## 快速支持：

{% embed url="https://sqs.senki.top/kms/" %}
S-QS/KMS
{% endembed %}

## 使用：

### 直接激活：

若您只想简简单单激活，您可以直接通过快速支持下载激活脚本运行。

### 手动激活：

千木社的KMS服务与其它的KMS服务无区别，将原有的kms地址替换成千木社kms地址即可

## Tip：

如果因各种原因需要清除，撤销激活状态和激活信息的，请以管理员身份在cmd中运行如下三条命令

```
slmgr /upk
slmgr /ckms
slmgr /rearm
```
