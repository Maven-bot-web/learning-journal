# 前 90 天逐周计划

这份计划把 12 个月路线压缩成前 90 天可执行版本。

原则：每周都要产出一个可运行、可测试或可解释的东西。

## Month 1：Linux + Git + Python 起步

### Week 1：Linux 基础体检 + Git 工作流

目标：能看懂一台 Linux 机器的基本状态，并完成 Git 提交。

学习：

- Linux 目录结构
- `df`、`free`、`ps`、`ss`、`ip`
- Git add / commit / push

产出：

- `health_check.sh` 初版
- `learning-journal` 第一周复盘
- `infra-ops-lab` README 初版

验收：

- 能解释 `df -h`、`free -m`、`ps -ef`、`ss -lntp` 的用途
- 能把修改提交并 push 到 GitHub

### Week 2：Shell 基础 + health_check 升级

目标：把手动命令整理成更可靠的脚本。

学习：

- Shell 变量
- `if`
- `for`
- 管道
- `grep`
- 退出码

产出：

- `health_check.sh` 升级版
- 增加清晰分区输出
- 增加基础错误处理

验收：

- 脚本可以重复运行
- 输出可读
- 出错时有提示

### Week 3：Python 基础 + system_check 初版

目标：用 Python 重写一部分系统检查能力。

学习：

- Python 基础语法
- list / dict
- 函数
- subprocess
- JSON 输出

产出：

- `src/system_check.py`
- 输出系统基本信息
- 输出 JSON 雏形

验收：

- 能运行 `python3 src/system_check.py`
- 能得到结构化输出

### Week 4：文件处理 + 日志读取

目标：让 Python 能读取文件并筛选关键信息。

学习：

- 文件读写
- 字符串处理
- 正则基础
- 异常处理

产出：

- `src/log_parser.py` 初版
- 示例日志文件
- 提取包含 `ERROR` 的行

验收：

- 能读取日志文件
- 能输出 ERROR 行数和内容
- 文件不存在时能给出错误提示

## Month 2：Python 工具化 + API + Docker 起步

### Week 5：日志字段解析 + JSON / CSV 输出

目标：从“筛选日志”升级到“结构化日志”。

学习：

- regex
- JSON
- CSV
- datetime 基础

产出：

- 解析时间、IP、级别、消息字段
- 输出 JSON
- 输出 CSV

验收：

- 输入日志文件，输出结构化结果

### Week 6：CLI 参数 + logging

目标：把脚本变成可用的小工具。

学习：

- argparse
- logging
- pathlib
- 配置文件基础

产出：

- `python src/log_parser.py --input sample.log --format json`
- 日志文件输出
- README 运行说明

验收：

- 参数错误时有提示
- 运行过程有日志

### Week 7：HTTP / API Checker

目标：用 Python 检查 HTTP 服务可用性。

学习：

- requests
- HTTP 状态码
- 超时
- 异常处理

产出：

- `src/api_checker.py`
- 支持检查多个 URL
- 输出状态码和耗时

验收：

- 能区分成功、超时、连接失败、非 200 状态

### Week 8：Docker 初步

目标：把 Python 工具放进容器运行。

学习：

- Image
- Container
- Dockerfile
- docker build
- docker run
- docker logs

产出：

- `Dockerfile`
- 容器内运行 `log_parser.py` 或 `api_checker.py`

验收：

- 不依赖本机 Python 环境，也能通过 Docker 运行工具

## Month 3：项目结构 + 测试 + Compose + AI 雏形

### Week 9：项目结构整理

目标：把零散脚本整理成项目结构。

学习：

- Python 包结构
- requirements.txt
- config 目录
- README 运行说明

产出：

```text
infra-ops-lab/
├── src/
├── tests/
├── config/
├── samples/
├── Dockerfile
└── README.md
```

验收：

- 新人看 README 能跑起来

### Week 10：测试与重构

目标：让代码可验证。

学习：

- pytest 基础
- 函数拆分
- 测试样例

产出：

- `tests/`
- 至少 3 个测试用例

验收：

- 本地能运行测试
- GitHub 里能看到测试说明

### Week 11：Docker Compose + 简单服务组合

目标：理解多个服务如何一起运行。

学习：

- compose.yaml
- volume
- port
- network
- service logs

产出：

- `compose.yaml`
- 一个 Python 服务或工具容器
- 一个辅助服务，例如 Nginx 或数据库雏形

验收：

- `docker compose up` 能启动
- 能查看日志
- 能解释服务之间如何通信

### Week 12：AI Incident Summary 雏形

目标：把 AI 接进已有工程流程，但只做一个小闭环。

学习：

- LLM API 基础
- Prompt 输入输出
- JSON 结构化结果
- 错误处理

产出：

- `src/ai_incident_summary.py`
- 输入异常日志
- 输出事故摘要：现象、可能原因、建议检查项

验收：

- 能对一段日志生成结构化摘要
- API 失败时有清晰错误提示

## 90 天结束时应该具备的结果

代码侧：

- 一个持续演进的 `infra-ops-lab`
- Shell health check
- Python system check
- Python log parser
- Python API checker
- Dockerfile
- Compose 初版
- AI incident summary 初版

记录侧：

- `learning-journal` 有 12 周复盘
- `PROGRESS.md` 能体现验收进度
- `projects/infra-ops-lab.md` 能说明项目演进
- 每周至少一次有效 commit

能力侧：

- 能独立使用 Linux 做基础排查
- 能写 Python 小工具
- 能用 GitHub 管理项目
- 能把脚本放进 Docker
- 能写 README 说明运行方式
- 能围绕日志、API、故障摘要做一个小闭环
