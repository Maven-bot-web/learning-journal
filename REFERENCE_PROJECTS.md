# 参考项目与使用方式

这份文档记录可以参考的 GitHub 学习项目，以及它们在当前路线里的作用。

原则：只借鉴记录方法和实验题，不照搬别人的路线。

## 推荐参考项目

| 项目 | 适合参考什么 | 推荐度 |
|---|---|---|
| `epic-aditya/learning-journal` | 阶段规划、周进度、验收标准、项目里程碑 | 五星 |
| `adiati98/learning-journal-template` | 学习日志模板、目录组织、记录格式 | 五星 |
| `kodekloudhub/100-days-of-devops` | Linux、Git、Docker、K8s、CI/CD、Ansible、Terraform 的实操任务库 | 四星 |
| `roadmap.sh/developer-roadmap` | 查知识地图、发现遗漏知识点 | 三星 |
| 各类 `100-Days-of-DevOps` | 参考每天或每周如何写实验记录 | 三星 |

## 各项目怎么用

### epic-aditya/learning-journal

地址：<https://github.com/epic-aditya/learning-journal>

适合参考：

- 如何把职业转型拆成阶段
- 如何写 `PROGRESS.md`
- 如何设置验收标准
- 如何记录项目里程碑

不适合照搬：

- 他的认证路线
- 他的时间表
- 他的 AWS / Security+ 优先级

原因：他的背景和目标不完全等于我的背景。我的主线是从网络安全产品交付，转向 DevOps / Platform / SRE / Cloud Security。

### adiati98/learning-journal-template

地址：<https://github.com/adiati98/learning-journal-template>

适合参考：

- 学习日志模板
- 目录组织方式
- 记录格式

不适合照搬：

- 具体内容
- 学习主题

### KodeKloud 100 Days of DevOps

地址：<https://github.com/kodekloudhub/100-days-of-devops>

适合参考：

- Linux 实操任务
- Git 实操任务
- Docker 实操任务
- Kubernetes / Jenkins / Ansible / Terraform 的后续题库

使用方式：

```text
当成实验题库，不当成总路线。
```

也就是说，我们先按自己的 12 周和 12 个月路线推进；需要实操题时，再从这里挑任务。

### roadmap.sh / developer-roadmap

地址：<https://roadmap.sh>

适合参考：

- 查知识地图
- 确认有没有明显遗漏
- 看某个方向的知识边界

不适合直接当计划。

原因：范围太大，容易重新掉进“什么都想学”的陷阱。

## 为什么不直接跟 100 Days 项目

我不是在做连续 100 天打卡，而是在做 1 年职业转型记录。

所以核心不是：

```text
今天打卡了吗？
```

而是：

```text
这周多了什么可运行的东西？
这个东西证明了我哪项能力？
```

## 推荐采用的最终模式

```text
我们制定路线
↓
learning-journal 负责记录
↓
KodeKloud / GitHub 项目提供部分实验
↓
infra-ops-lab 负责项目验收
```

## 当前仓库命名说明

当前仓库使用：

```text
learning-journal
```

它不是普通学习笔记，而是职业转型记录仓库。

如果以后要改名，可以考虑：

```text
engineering-learning-roadmap
devops-platform-learning
```

但当前阶段不急着改名，先把内容和节奏跑起来更重要。

## PROGRESS.md 的写法原则

不要写：

```text
[ ] 学习 Python
[ ] 学习 Linux
[ ] 学习 Git
```

这种无法验收。

应该写成：

```text
Linux
[ ] 能独立查看 IP / 路由 / 端口
[ ] 能定位进程和服务
[ ] 能查看和筛选日志
[ ] 能判断 CPU / 内存 / 磁盘问题

Python
[ ] 能读取文本文件
[ ] 能解析 JSON
[ ] 能处理异常
[ ] 能调用 HTTP API
[ ] 完成一个日志解析工具

Git
[ ] 能 clone / add / commit / push
[ ] 能建立 branch
[ ] 所有学习代码通过 Git 管理

验收项目
[ ] log-parser v1
```

核心是从“学过什么”改成“能做到什么”。

## 每周记录原则

每周只更新一次也可以，但要有产出。

示例：

```text
2026-W41

本周目标：
Python 文件处理 + Git

完成：
- list / dict
- 文件读取
- git commit / push

产出：
python/log_parser_v0.1.py

遇到的问题：
正则提取 JSON 失败

解决：
理解 greedy / non-greedy

下周：
异常处理 + JSON 解析
```

一年以后，GitHub commit history 本身应该能看出我的成长轨迹：

```text
Week 1  Linux lab
Week 2  Python parser v0.1
Week 3  parser v0.2
Week 4  API client
Week 5  Dockerfile
Week 6  Compose
```

这比突然上传一个“简历项目”更可信。
