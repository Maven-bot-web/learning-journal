# 复习机制参考项目

这份文档记录 GitHub 上可以参考的复习、学习记录和间隔重复项目。

原则：只借鉴机制，不把当前仓库改成复杂学习软件。

## 参考项目分类

| 类型 | 代表项目 | 适合参考什么 | 当前是否采用 |
|---|---|---|---|
| 学习日志模板 | `adiati98/learning-journal-template` | 目标、周记录、Markdown 记录方式 | 采用 |
| 开发者学习路线 | `danieldev-hub/full-stack-developer-learning-path` | 主动学习、项目驱动、间隔复习原则 | 部分采用 |
| 间隔复习工具 | `dhana-sekhar/spaced-repetition` | 1/3/7/14/30 等复习间隔、CSV 记录 | 部分采用 |
| 复杂学习系统 | `ZZyyHH2332/study-planner` | 到期复习、掌握状态、学习工作台 | 暂不采用复杂实现 |
| AI 学习平台 | `OrangJaguar/Veridian`、`ShiyunXu/studypilot` | 主动回忆、个性化复习、学习反馈循环 | 只参考思想 |
| Retention Log 系统 | `EmanHerawy/learnStack` | 用固定日志记录回忆结果和掌握程度 | 简化采用 |

## 可以直接借鉴的机制

### 1. 学习日志模板

参考项目：`adiati98/learning-journal-template`

可借鉴：

- 用 Markdown 记录学习过程
- 先声明目标，再记录进度
- 通过模板保持记录格式稳定

当前采用方式：

```text
weekly/
templates/weekly-review.md
PROGRESS.md
```

我们不直接复制模板，而是保留适合职业转型的字段：目标、构建、排障、输出、复盘。

## 2. 主动学习 + 项目驱动 + 间隔复习

参考项目：`danieldev-hub/full-stack-developer-learning-path`

可借鉴：

```text
主动学习：不要只看，要动手写
间隔复习：概念需要多次回看
项目驱动：通过真实项目巩固
调试：从错误中学习
公开构建：用 GitHub 留痕
```

当前采用方式：

```text
学习一个主题
↓
在 infra-ops-lab 做出功能
↓
在 learning-journal 记录复盘
↓
按 1-3-7-14-30 节奏复习
```

## 3. 间隔复习间隔

参考项目：`dhana-sekhar/spaced-repetition`

它使用预设间隔来安排复习，例如：

```text
1 天
3 天
7 天
14 天
30 天
60 天
90 天
180 天
365 天
```

当前采用简化版：

```text
当天
第 3 天
第 7 天
第 14 天
第 30 天
```

原因：当前重点不是考试记忆，而是工程能力。前 30 天内能不能复现和用到项目里，比长期背诵更重要。

## 4. 掌握状态

参考项目：`ZZyyHH2332/study-planner`

它有类似这样的状态流转：

```text
pending → in_progress → reviewed → mastered
```

当前采用简化版：

```text
未开始
学习中
已复习
可独立使用
```

建议在 `PROGRESS.md` 或周复盘里使用。

## 5. Retention Log

参考项目：`EmanHerawy/learnStack`

可借鉴：用统一格式记录一次复习是否真的回忆成功。

当前可以采用一个轻量文件：

```text
RETENTION_LOG.md
```

但暂时不强制创建，先把复习记录放在 `weekly/` 里。

如果后续内容多了，再升级成单独文件。

建议格式：

```text
日期：
主题：
复习方式：重跑 / 重写 / 复述 / 排障
结果：0-10 分
是否能独立使用：是 / 否
下次复习：
```

## 不采用的部分

当前不采用这些复杂能力：

```text
完整 Web 学习平台
自动生成题目
复杂掌握度算法
FSRS / IRT / BKT 模型
AI 自动排课
可视化学习仪表盘
```

原因：这些会把重点从“学习工程能力”转移到“维护学习系统”。

当前阶段只需要：

```text
轻量 Markdown
固定复习节奏
周复盘
项目验收
GitHub 记录
```

## 当前复习系统最终形态

```text
REVIEW_PLAN.md
定义复习原则和节奏

weekly/
记录每周复习结果

PROGRESS.md
更新能力验收状态

projects/infra-ops-lab.md
记录项目能力是否真正落地

notes/
只沉淀真正复习后仍有价值的知识
```

## 适合我的复习闭环

```text
学一个主题
↓
做一个可运行产出
↓
当天写记录
↓
第 3 天重跑
↓
第 7 天小练习
↓
第 14 天不看笔记复现
↓
第 30 天放进 infra-ops-lab 使用
↓
更新 PROGRESS.md
```

这套方式比单纯使用 Anki 或背诵工具更适合当前目标。

因为我的目标不是考试，而是形成可展示的工程能力。
