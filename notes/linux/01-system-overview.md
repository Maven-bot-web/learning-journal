# Linux 系统概览

进入一台 Linux 机器后，第一步不是急着操作，而是先判断这台机器是什么环境。

## 常用命令

```bash
cat /etc/os-release
uname -a
hostname
uptime
```

## 命令作用

`cat /etc/os-release` 用来查看 Linux 发行版信息。

`uname -a` 用来查看内核和系统架构信息。

`hostname` 用来查看机器名。

`uptime` 用来查看系统运行时间和负载。

## 我的理解

一台 Linux 机器可以从几个角度体检：

```text
系统：操作系统、内核、主机名、运行时间
存储：磁盘、挂载点、剩余空间
内存：总量、已用、可用
网络：IP、路由、网关、端口
进程：当前跑了哪些程序
```

先建立整体视角，再进入细节。
