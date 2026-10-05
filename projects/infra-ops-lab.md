# 项目记录：infra-ops-lab

## 项目定位

`infra-ops-lab` 是我的工程练习主项目，用来把 Linux、Shell、Python、API、Docker、CI/CD、排障和 AI 集成能力串起来。

`learning-journal` 只记录这个项目的目标、进度、复盘和问题，不复制项目代码。

## 项目目标

从一个简单的 Linux 体检脚本开始，逐步演进成一个小型运维工具集。

长期目标：

```text
系统检查
↓
日志解析
↓
API 检查
↓
测试
↓
容器化
↓
CI
↓
故障复盘
↓
AI 事故摘要
```

## 当前版本

当前已完成：

- Debian WSL2 环境准备
- 基础工具安装
- `health_check.sh` 初版
- Git 仓库初始化

## 12 周里程碑

| 周次 | 目标 | 项目产出 |
|---|---|---|
| Week 1 | Linux + Git | README、Linux lab notes |
| Week 2 | Shell | 升级 `health_check.sh` |
| Week 3 | Python | `src/system_check.py` |
| Week 4 | 文件 / JSON / 日志 | `src/log_parser.py` |
| Week 5 | HTTP / API | `src/api_checker.py` |
| Week 6 | 测试与重构 | `tests/` |
| Week 7 | Docker | `Dockerfile` |
| Week 8 | Compose | `compose.yaml` |
| Week 9 | Nginx / 网络 | `nginx/` |
| Week 10 | CI | GitHub Actions |
| Week 11 | 排障 | `docs/troubleshooting.md` |
| Week 12 | AI | `src/ai_incident_summary.py` |

## 学习记录规则

项目代码、配置和测试放在 `infra-ops-lab`。

学习解释、周复盘、问题记录放在 `learning-journal`。

如果某个问题来自 `infra-ops-lab`，在这里记录：

```text
问题现象：
判断过程：
验证方式：
根因：
解决方式：
关联 commit：
```

## 下一步

- 优化 `infra-ops-lab` README
- 升级 `health_check.sh` 输出格式
- 为 Week 1 写第一份周复盘
