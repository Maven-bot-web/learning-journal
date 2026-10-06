# Progress

这个文件只记录可验收能力，不记录“看过什么课程”。

## Phase 0 — Environment

状态：Completed

- [x] WSL2 Debian environment ready
- [x] Git installed and configured
- [x] Python / pip / venv installed
- [x] Basic tools installed: curl, vim, tree
- [x] `learning-journal` created
- [x] `learning-journal` pushed to GitHub
- [x] `infra-ops-lab` initialized
- [x] Basic `health_check.sh` created

## Week 1 — Linux + Git

状态：In Progress

Linux：

- [ ] 能解释 Linux 基础目录结构
- [ ] 能查看磁盘和内存状态
- [ ] 能查看进程
- [ ] 能查看监听端口
- [ ] 能查看 IP 和路由
- [ ] 能解释 WSL2 和 Windows 网络的基本关系

Git：

- [x] 能完成 `git add / commit / push`
- [x] 能连接 GitHub 远程仓库
- [ ] 能解释工作区、暂存区、本地提交、远程仓库
- [ ] 能写清晰 commit message

Deliverable：

- [ ] 优化 `infra-ops-lab` README
- [ ] 确认 `health_check.sh` 当前能力
- [ ] 写 Week 1 周复盘

## Week 2 — Shell + System Health Checking

状态：Not Started

- [ ] 能使用 Shell 变量
- [ ] 能使用 `if`
- [ ] 能使用 `for`
- [ ] 能理解退出码
- [ ] 能使用管道组合命令
- [ ] 能改进 `health_check.sh` 输出
- [ ] 能给脚本增加基础错误处理

Deliverable：

- [ ] `health_check.sh` v2

## Week 3 — Python + system_check

状态：Not Started

- [ ] 能写 Python 函数
- [ ] 能使用 list / dict
- [ ] 能调用系统命令
- [ ] 能输出 JSON
- [ ] 能处理基础异常

Deliverable：

- [ ] `src/system_check.py`

## Week 4 — Files / JSON / Logging + log_parser

状态：Not Started

- [ ] 能读取文本文件
- [ ] 能筛选 ERROR 日志
- [ ] 能解析时间、IP、级别、消息字段
- [ ] 能输出 JSON / CSV
- [ ] 能处理文件不存在等异常

Deliverable：

- [ ] `src/log_parser.py`

## Week 5 — HTTP / API + api_checker

状态：Not Started

- [ ] 能调用 HTTP API
- [ ] 能处理 JSON 响应
- [ ] 能处理超时
- [ ] 能处理连接失败
- [ ] 能记录请求结果

Deliverable：

- [ ] `src/api_checker.py`

## Week 6 — Testing + Refactoring

状态：Not Started

- [ ] 能写基础测试
- [ ] 能运行测试
- [ ] 能拆分函数
- [ ] 能整理项目结构

Deliverable：

- [ ] `tests/`

## Week 7 — Docker

状态：Not Started

- [ ] 能解释 image / container
- [ ] 能写 Dockerfile
- [ ] 能 build image
- [ ] 能 run container
- [ ] 能查看 logs

Deliverable：

- [ ] `Dockerfile`

## Week 8 — Docker Compose

状态：Not Started

- [ ] 能写 compose.yaml
- [ ] 能理解 service / volume / network
- [ ] 能使用 `docker compose up`
- [ ] 能排查服务日志

Deliverable：

- [ ] `compose.yaml`

## Week 9 — Nginx / Reverse Proxy / Service Networking

状态：Not Started

- [ ] 能解释反向代理
- [ ] 能理解端口映射
- [ ] 能排查服务访问失败

Deliverable：

- [ ] `nginx/`

## Week 10 — CI Pipeline

状态：Not Started

- [ ] 能理解 GitHub Actions 基础流程
- [ ] 能 push 后自动运行检查
- [ ] 能看懂 CI 失败原因

Deliverable：

- [ ] `.github/workflows/ci.yml`

## Week 11 — Failure Injection + Troubleshooting

状态：Not Started

- [ ] 能主动制造一个故障
- [ ] 能记录现象
- [ ] 能提出判断
- [ ] 能验证假设
- [ ] 能写出根因和解决方式

Deliverable：

- [ ] `docs/troubleshooting.md`

## Week 12 — AI Incident Summary

状态：Not Started

- [ ] 能调用 LLM API
- [ ] 能输入日志或故障文本
- [ ] 能输出结构化事故摘要
- [ ] 能处理 API 失败

Deliverable：

- [ ] `src/ai_incident_summary.py`
