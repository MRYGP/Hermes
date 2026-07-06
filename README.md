# SK Agent OS 学习台

这个仓库用于系统学习和沉淀个人 Agent 操作系统的设计方法。

当前定位不是“再造一个代码助手”，也不是把 Hermes 当成主力生产工具，而是：

> 以 Hermes 为样本，理解长期个人 Agent 如何管理记忆、技能、配置、自动化、调度、边界、成本与安全；同时用 Codex / Claude Code 做现实对照，判断哪些能力已经被主流工具覆盖，哪些能力仍值得自己掌握。

## 工具分工

| 工具 | 当前角色 |
| --- | --- |
| Codex | 主力仓库治理、代码修改、补丁生成、审查、自动化执行 |
| Claude Code | 复杂代码理解、大范围重构、工程型协作 |
| ChatGPT Project | 学习、复盘、路线设计、知识沉淀 |
| Hermes | Agent OS 机制实验台，不默认作为主力执行器 |

## 仓库结构

```text
.
├── README.md
├── docs/
│   ├── 00_项目定位.md
│   ├── 01_Agent_OS_学习地图.md
│   ├── 02_工具分工对照表.md
│   ├── 03_Hermes_关键概念速查.md
│   ├── 04_SK_仓库实战映射.md
│   ├── 05_自动化优先级清单.md
│   ├── 06_7到14天学习计划.md
│   ├── 07_记忆技能规则边界.md
│   └── 08_排错与省Token手册.md
├── project/
│   ├── ChatGPT_Project_Instructions.md
│   ├── Knowledge_Files_Checklist.md
│   └── SK_Agent_OS_学习台_GPTS_设计稿.md
└── templates/
    ├── skill_template.md
    ├── quick_command_template.md
    └── automation_audit_template.md
```

## 第一阶段目标

第一阶段只追求一个最小闭环：

1. 说明 Agent OS 是什么，以及为什么现在还要学 Hermes。
2. 建立 Codex / Claude Code / Hermes / ChatGPT Project 的分工。
3. 把 Hermes 的核心概念映射到 SK 仓库的真实动作。
4. 形成 7-14 天学习计划。
5. 沉淀第一批可复用模板：skill、quick command、自动化审计。

## 当前学习原则

- 先学可迁移能力，不追求 Hermes 全功能。
- 先跑手动流程，再做自动化。
- 先固定规则，再固定动作。
- 先用 Codex / Claude Code 做执行，再用 Hermes 理解系统结构。
- 不把短期状态长期写进知识库。

## 下一步

从 [docs/00_项目定位.md](docs/00_项目定位.md) 开始读，然后执行 [docs/06_7到14天学习计划.md](docs/06_7到14天学习计划.md) 的第 1 天任务。
