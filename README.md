# SK Agent OS 学习台

## 一句话定位

**SK Agent OS 学习台** 是一个个人 Agent 工作流学习仓库。

它研究的不是某一个具体产品，而是一个人如何长期组织 AI 的上下文、规则、技能、工具、自动化、权限、安全和成本。

## 当前阶段

当前 v2 阶段优先学习“ChatGPT 工作台”。

“ChatGPT 工作台”是本仓库术语，不是 OpenAI 官方产品名称。它用于组织当前可观察到的 Chat、Work、Project、Codex、Plugins、Apps、Scheduled Tasks 等工作方式。

Hermes 保留为 Agent OS 机制教材与对照实验台，不默认作为主力生产工具。

## 当前工具分工

| 工具 | 当前角色 |
| --- | --- |
| Chat | 快速讨论、轻量判断、临时解释 |
| Work | 长任务、研究分析、成品交付 |
| Project | 学习、复盘和稳定知识组织 |
| Codex | 本地仓库读取、文件修改、命令执行和验证 |
| Claude Code | 复杂工程理解、大范围重构和第二视角协作 |
| Hermes | Agent OS 机制教材与对照实验台 |
| Plugin | 工作流包装和发现 |
| App | 外部数据、工具和动作连接 |
| Scheduled Task | 周期提醒、简报和低风险监测 |

## 仓库结构

```text
.
├── AGENTS.md
├── PROJECT_STATE.md
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
│   ├── 08_排错与省Token手册.md
│   ├── 09_官方资料索引与复核清单.md
│   └── 10_ChatGPT_工作台能力地图.md
├── project/
│   ├── ChatGPT_Project_Instructions.md
│   ├── ChatGPT_Project_Setup.md
│   ├── Knowledge_Files_Checklist.md
│   ├── SK_Agent_OS_学习台_GPTS_设计稿.md
│   └── Repository_Knowledge_Sync_Protocol.md
├── templates/
├── examples/
├── logs/
└── archive/
```

## 从哪里开始

1. [PROJECT_STATE.md](PROJECT_STATE.md)
2. [docs/00_项目定位.md](docs/00_项目定位.md)
3. [docs/06_7到14天学习计划.md](docs/06_7到14天学习计划.md)
4. [docs/10_ChatGPT_工作台能力地图.md](docs/10_ChatGPT_工作台能力地图.md)

## 本地仓库与 ChatGPT Project

本地仓库是 source of truth。

`PROJECT_STATE.md` 是当前进度入口。ChatGPT Project 是学习、复盘和知识组织中心，其中的上传文件只是快照，不会自动等同于本地最新状态。

长期稳定知识按 [project/Knowledge_Files_Checklist.md](project/Knowledge_Files_Checklist.md) 上传。每次阶段性修改后，按 [project/Repository_Knowledge_Sync_Protocol.md](project/Repository_Knowledge_Sync_Protocol.md) 同步。

## 当前不做什么

- 不把仓库长期定位改成某个具体产品学习仓库。
- 不把“ChatGPT 工作台”写成 OpenAI 官方产品名。
- 不追求系统学完 Hermes 全功能。
- 不把 Hermes 设计成主力仓库执行器。
- 不把频繁变化的状态放进长期知识库。
- 不让自动化样例默认写入仓库。
