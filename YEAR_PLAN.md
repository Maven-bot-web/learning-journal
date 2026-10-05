# 12 个月学习规划

这份规划用来把长期目标、阶段目标、周计划和验收标准串起来。

学习不再按“看完多少课程”衡量，而是按“能做出什么东西”衡量。

## 学习规划四层结构

```text
学习规划
├── 年度目标：12 个月后具备什么能力
├── 阶段目标：每 2 到 3 个月解决一个能力层级
├── 周计划：每周具体学什么、做什么
└── 验收标准：不是学完课程，而是能做出什么
```

## 第 1 阶段：0 到 2 个月

重点：Linux + Python + Git + Shell 基础。

目标不是学深，而是跨过“不会写程序”的门槛。

学习内容：

```text
Linux
├── 文件 / 权限
├── 进程 / 服务
├── 网络
├── 日志
└── 磁盘 / 内存

Python
├── 基础语法
├── list / dict
├── 函数
├── 文件处理
├── 异常处理
├── JSON
└── requests

Shell
├── 变量
├── if
├── for
├── 管道
└── grep / awk / sed

Git
├── clone
├── add / commit
├── branch
├── merge
└── GitHub
```

阶段验收：

```text
Python 程序
↓
读取一个日志文件
↓
提取 ERROR
↓
解析 IP / 时间 / 字段
↓
输出 JSON / CSV
```

以及：

```text
Python
↓
调用一个 HTTP API
↓
处理 JSON 响应
↓
处理异常
↓
写日志
```

做到这些，再进入下一阶段。

## 第 2 阶段：2 到 4 个月

重点：Python 实际应用 + API + Docker。

这个阶段 Python 开始从语言变成工具。

学习内容：

```text
Python
├── requests
├── pathlib
├── logging
├── argparse
├── subprocess
├── regex
├── CSV / Excel
└── 基础并发

Docker
├── Image
├── Container
├── Dockerfile
├── Volume
├── Port
├── Network
├── docker logs
├── docker exec
└── docker inspect
```

项目 1：日志处理服务。

第一版：

```text
日志文件
↓
Python
↓
结构化 JSON
```

第二版：

```text
日志
↓
Python Parser
↓
保存数据库
```

第三版：

```text
Python 程序
↓
Docker
```

这个阶段不需要一开始上 Kafka 或 Kubernetes，先让它真正跑起来。

## 第 3 阶段：4 到 6 个月

重点：软件工程 + Docker Compose + CI/CD。

从这个阶段开始，不能再只写零散脚本，要学习真正的项目结构。

示例结构：

```text
project/
├── app/
│   ├── parser.py
│   ├── api.py
│   └── config.py
├── tests/
├── config/
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── README.md
```

学习内容：

```text
配置管理
日志
测试
异常处理
环境变量
依赖管理
```

CI/CD 基础流程：

```text
Git Push
↓
自动测试
↓
Build Docker Image
↓
部署
```

AI 从这个阶段开始正式进入项目，不单独开一条孤立课程。

示例：

```text
日志
↓
Python 解析
↓
异常日志
↓
LLM API
↓
生成故障摘要
```

## 第 4 阶段：6 到 9 个月

重点：Kubernetes + Observability。

这个阶段应该已经有一个真实服务，再用它学习 Kubernetes。

学习内容：

```text
Kubernetes
├── Pod
├── Deployment
├── Service
├── ConfigMap
├── Secret
├── Ingress
├── PVC
└── Troubleshooting
```

暂时不急着学习 Operator、CRD、Service Mesh。

目标是把自己的项目部署进去：

```text
Python Parser
+
API Service
+
ClickHouse
+
Grafana
```

同时开始理解：

```text
Prometheus
Grafana
Logs
Metrics
```

核心问题：为什么系统需要可观测性。

## 第 5 阶段：9 到 12 个月

重点：Cloud + Terraform + AI 工程化。

学习内容：

```text
Cloud
├── VM
├── VPC
├── Subnet
├── Security Group
├── IAM
├── Load Balancer
└── Object Storage
```

Terraform：

```text
代码
↓
创建基础设施
↓
部署服务
```

AI 继续向这些方向发展：

```text
RAG
Tool Calling
Agent
Evaluation
Vector DB
LLM Gateway
```

但 AI 仍然围绕主项目，不单独游离。

最终项目可以演进成：

```text
Security Log Platform
├── 日志输入
├── Kafka
├── Python Parser
├── ClickHouse
├── API
├── Grafana
├── AI 分析
├── Docker
├── CI/CD
├── Kubernetes
└── Monitoring
```

## 学习时间分配

初期：

```text
Python      35%
Linux       25%
网络深化    15%
Git/Shell   15%
AI          10%
```

3 个月以后：

```text
Python / 项目   30%
Docker          25%
Linux           15%
Git / CI/CD     15%
AI              15%
```

6 个月以后：

```text
项目          30%
K8s           25%
Docker/CI     15%
Linux/网络    15%
AI            15%
```

## 每周学习方式

不要按课程切碎：

```text
周一 Python 课
周二 Linux 课
周三 Docker 课
周四 AI 课
```

建议围绕一个任务学习。

例如：

```text
本周任务：让 Python 成功解析一份日志
```

自然会碰到：

```text
Python
文件 IO
正则
JSON
异常处理
Git
```

下一周：

```text
把程序做成 CLI
```

自然会学：

```text
argparse
logging
配置文件
```

再下一周：

```text
把它放进 Docker
```

这样所有知识会串起来。

## 进度衡量规则

不要用：

```text
今天学了两个小时
```

衡量进度。

要用：

```text
这周多了什么可运行的东西？
```

例子：

```text
Week 1：能读取日志
Week 2：能解析字段
Week 3：能调用 API
Week 4：能输出 CSV
Week 5：Docker 运行
Week 6：接数据库
```

如果连续四周都没有产生任何代码、配置、README 或运行结果，说明学习方式有问题。

## 第一阶段约束

第一阶段不要超过 8 周。

原因：最大的风险是基础一直学，项目始终不开。

所以：

```text
第 1 个月开始 Python
第 2 个月必须开始第一个小项目
```

不要等“Python 学得差不多了”才开始项目。

## 一年后的目标

一年以后，目标不是看完多少课程，而是具备这些能力：

```text
能独立使用 Linux
+
能写 Python 工具 / 服务
+
会 Git
+
能写 Dockerfile
+
能搭 CI/CD
+
能部署到 K8s
+
理解日志 / 监控
+
能调用并集成 LLM
+
有至少 1 到 2 个完整项目
```

这才是能支撑转岗的能力组合。
