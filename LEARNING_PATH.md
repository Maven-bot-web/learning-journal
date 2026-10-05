# 完整学习路径

这份路径用来回答三个问题：

```text
我现在在哪里？
下一步学什么？
学到什么程度才算过关？
```

当前主线不是单纯背命令，而是逐步建立一种能力：能在 Linux 环境里操作、排错、写脚本、理解网络，最后把这些能力迁移到云平台和安全场景。

## 总体路线

```text
阶段 0：环境准备
阶段 1：Linux 基础体检能力
阶段 2：Git 和命令行工作流
阶段 3：Bash 脚本自动化
阶段 4：网络基础
阶段 5：Python 自动化
阶段 6：云计算基础
阶段 7：安全基础
阶段 8：综合项目和作品集
```

## 阶段 0：环境准备

目标：准备一个稳定的学习环境。

要完成：

- Debian WSL2 可用
- Git 可用
- Python 3、pip、venv 可用
- curl、vim、tree 等基础工具可用
- GitHub 仓库可 push

过关标准：

- 能进入 Debian WSL2
- 能创建本地 Git 仓库
- 能提交并推送到 GitHub
- 知道 Windows 路径和 Linux 路径的区别

对应产出：

- `learning-journal` 仓库
- `infra-ops-lab` 仓库
- 第一条 GitHub 提交记录

## 阶段 1：Linux 基础体检能力

目标：拿到一台 Linux 机器后，能判断它的基本状态。

要学习：

- 系统版本：`cat /etc/os-release`
- 内核信息：`uname -a`
- IP 地址：`ip a`、`ip -brief address`
- 路由和网关：`ip route`
- 磁盘：`df -h`、`df -hT`
- 内存：`free -m`、`free -h`
- 进程：`ps -ef`
- 端口：`ss -lntp`

过关标准：

- 能解释每条命令的用途
- 能看懂命令输出里的关键字段
- 能判断“正常”和“需要关注”的情况
- 能写出一个基础 `health_check.sh`

对应产出：

- `notes/linux/01-system-overview.md`
- `notes/linux/02-disk-and-memory.md`
- `notes/linux/03-processes-and-ports.md`
- `labs/linux-health-check/README.md`
- `infra-ops-lab/health_check.sh`

## 阶段 2：Git 和命令行工作流

目标：把 Git 变成日常习惯，而不是临时工具。

要学习：

- `git status`
- `git add`
- `git commit`
- `git log`
- `git diff`
- `git remote -v`
- `git push`
- `.gitignore`

过关标准：

- 每天学习后能自己提交一次
- 能看懂工作区、暂存区、提交记录的区别
- 能知道本地仓库和 GitHub 远程仓库的关系
- 不把密钥、密码、token 提交到仓库

对应产出：

- `notes/git/01-basic-workflow.md`
- 每日 GitHub commit
- 清晰的提交信息

## 阶段 3：Bash 脚本自动化

目标：把重复命令整理成可复用脚本。

要学习：

- shebang：`#!/usr/bin/env bash`
- 变量
- 条件判断
- 循环
- 函数
- 参数
- 退出码
- 基础错误处理

过关标准：

- 能读懂简单 Bash 脚本
- 能把 3 条以上命令组合成脚本
- 能给脚本加执行权限
- 能解释脚本失败时大概哪里出问题

对应产出：

- `infra-ops-lab/health_check.sh` 升级版
- Bash 学习笔记
- Bash 小练习

## 阶段 4：网络基础

目标：理解本机、WSL2 和互联网之间的基本通信路径。

要学习：

- IP 地址
- 子网和 CIDR
- 默认网关
- NAT
- DNS
- TCP/UDP
- 端口
- HTTP/HTTPS
- 防火墙基本概念

过关标准：

- 能解释 WSL2 为什么有自己的 IP
- 能解释默认网关是什么
- 能看懂 `ss -lntp` 里的监听端口
- 能用 `curl` 做基本连通性测试
- 能画出“WSL2 -> Windows -> 网络”的简单路径

对应产出：

- `notes/networking/01-wsl2-network.md`
- 网络诊断实验
- WSL2 网络结构图

## 阶段 5：Python 自动化

目标：用 Python 写小工具，处理文件、日志和命令输出。

要学习：

- 虚拟环境：`python3 -m venv .venv`
- 文件读写
- JSON
- argparse
- subprocess
- logging
- exception handling

过关标准：

- 能创建和进入虚拟环境
- 能写一个带参数的 Python 脚本
- 能读取文件并输出简单报告
- 能调用系统命令并处理输出

对应产出：

- Python 学习笔记
- 简单日志分析脚本
- 系统检查报告生成器

## 阶段 6：云计算基础

目标：把本地 Linux 和网络知识迁移到云平台。

要学习：

- 云服务器是什么
- 对象存储是什么
- IAM 是什么
- VPC 是什么
- 安全组是什么
- 日志和监控是什么

过关标准：

- 能把 EC2 类比成本地 Linux 服务器
- 能把安全组类比成云上的防火墙规则
- 能解释 IAM 为什么重要
- 能理解 VPC、子网、路由表的基本关系

对应产出：

- 云计算基础笔记
- 第一个云架构图
- 第一个云实验记录

## 阶段 7：安全基础

目标：从“会用系统”走向“知道怎么让系统更安全”。

要学习：

- 用户和权限
- SSH 安全
- 最小权限原则
- 日志审计
- 防火墙
- 漏洞和补丁
- 密钥和凭据保护

过关标准：

- 不把密钥提交到 GitHub
- 能解释为什么 root 账号要谨慎使用
- 能看懂基本登录日志
- 能列出一台 Linux 机器的基础加固项

对应产出：

- Linux 安全检查清单
- SSH 安全笔记
- 基础加固脚本雏形

## 阶段 8：综合项目和作品集

目标：把学习记录变成可以展示的项目能力。

项目方向：

- Linux health check 工具
- 日志分析小工具
- 网络诊断脚本
- 云资源检查脚本
- 基础安全加固清单

过关标准：

- 每个项目有 README
- 能说明项目解决什么问题
- 能说明怎么运行
- 能展示一次真实输出
- GitHub commit 记录清晰

对应产出：

- `infra-ops-lab` 项目持续升级
- `learning-journal` 持续记录学习过程
- 1 到 3 个能展示的小项目

## 每天的学习闭环

每天不需要做很多，但要形成闭环：

```text
学一个概念
跑一组命令
记录一个现象
整理一段笔记
提交一次 Git
```

推荐节奏：

1. 先在 WSL 里动手操作
2. 把输出和问题发给 Codex
3. Codex 帮忙解释、整理、补文档
4. 自己复述一遍关键理解
5. 提交并 push 到 GitHub

## 仓库分工

`learning-journal`：记录学习路线、笔记、实验过程和每日总结。

`infra-ops-lab`：保存真正写出来的脚本、小工具和项目代码。

简单理解：

```text
learning-journal = 我怎么学会的
infra-ops-lab    = 我能做出什么
```
