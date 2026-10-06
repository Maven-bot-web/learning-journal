# Roadmap

当前路线只保留一个重点：前 12 周把基础工程能力跑通。

Kubernetes、Terraform、RAG、Agent 等内容放到后续阶段，不提前抢主线。

## Phase 0 — Environment

状态：已完成。

已具备：

- Windows + WSL2 + Debian
- Git / GitHub
- Python / pip / venv
- Shell 基础环境
- `learning-journal` 已推送到 GitHub
- `infra-ops-lab` 已有 `health_check.sh` 初版

## Week 1 — Linux + Git

目标：能在 Linux 中完成基础检查，并用 Git 管理修改。

产出：

- `infra-ops-lab` README 初版或优化版
- 确认 `health_check.sh` 当前输出
- 第一份周复盘

验收：

- 能解释 `df`、`free`、`ps`、`ss`、`ip route`
- 能完成 `git add / commit / push`

## Week 2 — Shell + System Health Checking

目标：把系统检查脚本做得更可靠。

产出：

- 升级 `health_check.sh`
- 增加清晰输出
- 增加基础错误处理

## Week 3 — Python + system_check

目标：用 Python 复现部分系统检查能力。

产出：

- `src/system_check.py`
- 结构化输出雏形

## Week 4 — Files / JSON / Logging + log_parser

目标：读取日志，解析错误，输出结构化结果。

产出：

- `src/log_parser.py`
- 示例日志
- JSON / CSV 输出

## Week 5 — HTTP / API + api_checker

目标：用 Python 检查 HTTP 服务可用性。

产出：

- `src/api_checker.py`
- 超时、异常、状态码处理

## Week 6 — Testing + Refactoring

目标：让项目可测试、可维护。

产出：

- `tests/`
- 基础测试用例
- 更清晰的项目结构

## Week 7 — Docker

目标：把工具放进容器运行。

产出：

- `Dockerfile`
- Docker 运行说明

## Week 8 — Docker Compose

目标：用 Compose 管理多个服务。

产出：

- `compose.yaml`
- 服务编排说明

## Week 9 — Nginx / Reverse Proxy / Service Networking

目标：理解服务网络和反向代理。

产出：

- `nginx/`
- 服务访问与排障记录

## Week 10 — CI Pipeline

目标：GitHub push 后自动检查项目。

产出：

- `.github/workflows/ci.yml`
- 自动测试或脚本检查

## Week 11 — Failure Injection + Troubleshooting

目标：主动制造故障并记录排障过程。

产出：

- `docs/troubleshooting.md`
- 至少 3 个故障案例

## Week 12 — AI Incident Summary

目标：把 AI 接入已有工程流程，生成结构化事故摘要。

产出：

- `src/ai_incident_summary.py`
- 输入日志或故障文本
- 输出现象、可能原因、建议检查项

## Next Stage

12 周后再进入：

```text
Observability：Prometheus / Grafana
Kubernetes
Cloud
Terraform
AI Engineering：RAG / Tool Calling / Agent
```
