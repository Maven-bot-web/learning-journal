# 执行模式

这套学习系统采用一个固定闭环：

```text
我们制定路线
↓
GitHub Learning Journal 负责记录
↓
KodeKloud / GitHub 项目提供部分实验
↓
你自己的项目负责验收
```

## 1. 我们制定路线

路线不是直接照搬某个课程或某个 100 Days 项目。

路线根据我的实际背景设计：

```text
当前基础：网络安全产品交付 / 实施
当前短板：软件工程、自动化、容器、云原生
目标方向：DevOps / Platform / SRE / Cloud Security
学习方式：围绕项目产出推进
```

路线文件主要是：

- `YEAR_PLAN.md`
- `FIRST_90_DAYS.md`
- `ROADMAP.md`
- `LEARNING_PATH.md`

这些文件回答：

```text
未来 12 个月怎么走？
前 90 天怎么落地？
当前阶段学什么？
学到什么程度算过关？
```

## 2. GitHub Learning Journal 负责记录

`learning-journal` 是记录仓库，不是代码主仓库。

它负责记录：

```text
为什么学
学什么
本周目标
本周产出
遇到的问题
怎么排障
是否达到验收标准
下一步做什么
```

核心文件：

- `PROGRESS.md`：验收进度
- `weekly/`：每周复盘
- `notes/`：真正沉淀下来的知识
- `projects/`：项目复盘和里程碑

它不负责堆代码，也不负责复制教程。

## 3. KodeKloud / GitHub 项目提供部分实验

外部项目不是主线，只是题库和参考资料。

例如：

```text
KodeKloud 100 Days of DevOps
GitHub 上的 learning journal 项目
roadmap.sh
其他 100-Days-of-DevOps 仓库
```

它们的作用是：

```text
提供练习题
提供记录方式参考
帮助查漏补缺
提供项目结构灵感
```

它们不决定我的路线。

如果外部项目的任务和当前阶段匹配，就拿来做。

如果外部项目提前进入 Kubernetes、Terraform、Ansible，而我当前还在 Linux / Python / Docker 阶段，就先不做。

## 4. 自己的项目负责验收

真正证明能力的不是看完课程，而是自己的项目能不能跑。

当前主项目：

```text
infra-ops-lab
```

它负责承载：

```text
Shell 脚本
Python 工具
日志解析
API 检查
Docker
Compose
CI/CD
故障排查
AI 事故摘要
```

每一阶段最终都要落到 `infra-ops-lab` 的可运行产出上。

例如：

```text
学 Linux
↓
health_check.sh 能跑

学 Python 文件处理
↓
log_parser.py 能解析日志

学 API
↓
api_checker.py 能检查 HTTP 服务

学 Docker
↓
工具能在容器里跑

学 CI/CD
↓
GitHub push 后能自动测试
```

## 这个模式为什么适合我

我不是从零开始做纯开发，也不是单纯考证。

我是在从网络安全产品交付，转向更通用的工程能力。

所以最适合的方式不是：

```text
课程驱动
```

而是：

```text
项目驱动 + 每周记录 + 阶段验收
```

## 每周执行闭环

每周按这个顺序执行：

```text
1. 从路线里确定本周目标
2. 从外部项目挑合适实验，或者自己定义实验
3. 在 infra-ops-lab 里完成可运行产出
4. 在 learning-journal 里记录过程和复盘
5. 更新 PROGRESS.md 验收状态
6. commit + push
```

## 判断一周是否有效

有效的一周至少应该有一个结果：

```text
代码
配置
README
运行截图 / 输出
排障记录
周复盘
```

如果一周只有“看了很多资料”，但没有任何可运行、可测试、可解释的产出，就说明执行方式需要调整。
