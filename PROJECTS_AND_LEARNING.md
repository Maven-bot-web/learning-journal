# 项目分工与学习主线

这份文档用来说明：哪些仓库负责记录，哪些仓库负责动手学习，以及 `learning-journal` 后续应该优化成什么样。

## 一句话结论

```text
learning-journal = 职业转型控制台
infra-ops-lab    = 工程练习与项目仓库
```

不要把两个仓库混在一起。

`learning-journal` 负责回答：

```text
我为什么学？
我正在学什么？
我本周做到了什么？
我是否达到验收标准？
我下一步要做什么？
```

`infra-ops-lab` 负责回答：

```text
我能写什么脚本？
我能构建什么工具？
我能不能测试、部署、排障？
我有没有真实可运行的项目？
```

## 仓库分工

| 仓库 | 类型 | 主要作用 | 不应该放什么 |
|---|---|---|---|
| `learning-journal` | 记录仓库 | 路线、进度、周复盘、验收记录、项目复盘 | 大量代码、脚本实现、复制版教程 |
| `infra-ops-lab` | 学习/项目仓库 | Shell、Python、Docker、CI/CD、排障实验、AI 集成项目 | 大段学习日记、职业规划长文 |

## learning-journal 要优化成什么

`learning-journal` 不应该只是普通笔记本，也不应该只是课程目录。

它应该优化成：

```text
职业转型控制台
```

也就是打开仓库后，别人能快速看懂：

```text
当前背景是什么
目标方向是什么
当前阶段是什么
本周在做什么
已经完成了什么
每个阶段如何验收
最终产出有哪些项目
```

## learning-journal 的优化内容

### 1. README.md

定位：说明我是谁、为什么转型、当前目标是什么。

应该包含：

- 当前角色：网络安全产品交付 / 实施
- 当前问题：过度依赖厂商黑盒产品，工程能力需要迁移
- 目标方向：DevOps / Platform / SRE / Cloud Security
- 当前主线：Linux、Shell、Python、Git、API、Docker、CI/CD
- 学习原则：每周必须产出可运行、可测试或可解释的东西

### 2. ROADMAP.md

定位：12 周主线，不做大而全路线。

重点是当前阶段：

```text
Week 1  Linux + Git
Week 2  Shell + system health checking
Week 3  Python + system_check
Week 4  Files / JSON / logging + log_parser
Week 5  HTTP / API + api_checker
Week 6  Testing + refactoring
Week 7  Docker
Week 8  Docker Compose
Week 9  Nginx / reverse proxy / service networking
Week 10 CI pipeline
Week 11 Failure injection + troubleshooting
Week 12 AI Incident Summary
```

Kubernetes、Terraform、RAG、Agent 放到下一阶段，不提前抢主线。

### 3. PROGRESS.md

定位：验收表。

不要写成：

```text
[ ] 学习 Linux
[ ] 学习 Python
```

要写成：

```text
[ ] 能解释 Linux 目录结构
[ ] 能查看进程和端口
[ ] 能写 health_check.sh
[ ] 能把脚本提交到 GitHub
[ ] 能说明脚本解决什么问题
```

也就是：从“我学了什么”改成“我能做到什么”。

### 4. weekly/

定位：每周复盘。

不追求每天打卡，采用每周约 8 小时节奏：

```text
2h 学习
4h 构建
1h 故障注入 / 排障
1h 文档 / Git / 复盘
```

每周都要留下：目标、完成内容、遇到的问题、排障过程、下周计划。

### 5. notes/

定位：只记录真正有用的知识。

不写百科，不复制教程。

只记录三类内容：

```text
我容易忘的
我真正踩过的坑
我以后排障会用到的
```

### 6. projects/

定位：记录项目复盘，不放项目代码。

例如：

```text
projects/infra-ops-lab.md
```

里面记录：

- 项目目标
- 当前版本
- 架构演进
- 已完成能力
- 遇到的问题
- 学到的东西
- 下一步计划

## infra-ops-lab 用来学什么

`infra-ops-lab` 是真正动手的主项目。

它应该逐步演进成：

```text
infra-ops-lab/
├── scripts/
│   └── health_check.sh
├── src/
│   ├── system_check.py
│   ├── log_parser.py
│   ├── api_checker.py
│   └── ai_incident_summary.py
├── tests/
├── config/
├── nginx/
├── docs/
│   └── troubleshooting.md
├── Dockerfile
├── compose.yaml
└── .github/
    └── workflows/
        └── ci.yml
```

每一周都围绕这个项目加一层能力。

## 学习整体路线

### Phase 0：环境准备

目标：环境可用，GitHub 可同步。

产出：

- Debian WSL2
- Git / Python / Shell 环境
- `learning-journal`
- `infra-ops-lab`
- 第一次 commit + push

状态：已完成。

### Week 1：Linux + Git

目标：能在 Linux 里操作文件、看系统状态、完成 Git 提交。

产出：

- Linux 基础笔记
- Git 工作流笔记
- `infra-ops-lab` README 优化

### Week 2：Shell + 系统体检

目标：把手动命令整理成可靠脚本。

产出：

- 升级版 `health_check.sh`
- 可读输出
- 基础错误处理

### Week 3：Python + system_check

目标：用 Python 重写部分系统检查能力。

产出：

- `src/system_check.py`
- 基础 CLI 参数
- JSON 输出雏形

### Week 4：文件 / JSON / 日志

目标：能读取文件、解析日志、生成简单报告。

产出：

- `src/log_parser.py`
- 日志样例
- 解析结果说明

### Week 5：HTTP / API

目标：理解 API 调用和服务可用性检查。

产出：

- `src/api_checker.py`
- HTTP 状态检查
- 超时和异常处理

### Week 6：测试与重构

目标：让代码变得可验证、可维护。

产出：

- `tests/`
- 基础单元测试
- 项目结构整理

### Week 7：Docker

目标：把工具放进容器运行。

产出：

- `Dockerfile`
- 容器内运行检查脚本

### Week 8：Docker Compose

目标：用 Compose 管理多个服务。

产出：

- `compose.yaml`
- 示例服务
- 基础服务编排说明

### Week 9：Nginx / 反向代理 / 服务网络

目标：理解服务之间如何通信。

产出：

- `nginx/`
- 反向代理配置
- 网络排障记录

### Week 10：CI Pipeline

目标：让 GitHub 自动检查项目。

产出：

- `.github/workflows/ci.yml`
- 自动运行测试
- 自动检查脚本格式

### Week 11：故障注入与排障

目标：主动制造故障并记录排障过程。

产出：

- `docs/troubleshooting.md`
- 至少 3 个故障案例
- 现象、判断、验证、根因、解决

### Week 12：AI Incident Summary

目标：把 AI 接入工程流程，但不让 AI 抢主线。

产出：

- `src/ai_incident_summary.py`
- 输入日志或故障文本
- 输出结构化事故摘要

## 下一阶段

当前 12 周完成后，再进入：

```text
Observability
├── Prometheus
└── Grafana

Kubernetes

Cloud

Terraform

AI Engineering
├── RAG
├── Tool Calling
└── Agent
```

## 每周闭环

每周只追求一个清晰闭环：

```text
学一个主题
做一个功能
制造或遇到一个问题
记录一次排障
提交一次 GitHub
复盘一次收获
```

不要追求目录好看，要追求每周真的多一项能力。
