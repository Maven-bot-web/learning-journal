# 实验：Linux 基础体检

## 目标

建立进入一台 Linux 机器后的基础检查习惯。

## 环境

- Debian WSL2
- 用户：`mwf`
- 相关项目仓库：`~/infra-ops-lab`

## 手动检查命令

```bash
cat /etc/os-release
ip route
df -h
free -m
ps -ef | head
ss -lntp
```

## 检查内容

```text
系统版本和内核
IP 地址和路由
磁盘使用情况
内存使用情况
正在运行的进程
正在监听的端口
```

## 实验结果

第一个 `health_check.sh` 已经创建在 `~/infra-ops-lab`。

这个实验记录用来解释脚本背后的检查思路。脚本本身放在项目仓库里，学习过程和理解记录在这里。

## 后续改进

- 补充每条命令的解释。
- 再次运行脚本并记录输出。
- 对比手动命令输出和脚本输出。
