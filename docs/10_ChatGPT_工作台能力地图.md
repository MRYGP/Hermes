# ChatGPT 工作台能力地图

> “ChatGPT 工作台”是本仓库术语，不是 OpenAI 官方产品名称。
>
> 本文件记录当前阶段可观察到的 ChatGPT 工作方式。
> 产品名称、界面、套餐和能力可能发生变化。
>
> 最近官方复核：2026-07-10
> 建议下次复核：2026-08-09 前

本文件属于阶段性能力知识，不是永久产品定义，需要定期复核。

## 1. 为什么建立“ChatGPT 工作台”这一抽象层

当前 ChatGPT 相关能力分散在 Chat、Work、Project、Codex、Plugins、Apps、Scheduled Tasks、桌面应用和内置浏览器等 surface 中。

本仓库用“ChatGPT 工作台”作为学习抽象层，是为了回答：

```text
当前一个人到底应该在哪个 surface 完成哪类工作？
```

这个抽象层服务于学习，不替代官方产品名称。

## 2. 本仓库术语定义

“ChatGPT 工作台”当前统称：

- Chat
- ChatGPT Work
- ChatGPT Project
- ChatGPT Desktop
- Codex
- Plugins
- Apps
- Scheduled Tasks
- 内置浏览器
- Memory
- approvals / permissions

这些具体产品形态可能变化，因此不能写入仓库长期定位的核心定义。

## 3. Chat

1. 当前官方如何定义：面向即时对话、问答和轻量任务的 ChatGPT 基础交互 surface。
2. 适合解决什么问题：快速讨论、临时解释、轻量判断、短文案草稿。
3. 不适合解决什么问题：长时间仓库执行、大范围本地修改、自动维护项目状态。
4. 在 SK 仓库中映射成什么动作：提出方案、收敛问题、生成候选提示词或小段文案。
5. 当前账户是否已经实测：当前账户尚未在 Day 2 记录中实测。

## 4. ChatGPT Work

1. 当前官方如何定义：用于长任务、研究分析和成品交付的工作 surface，能力和可用性可能受 rollout、套餐、workspace 和平台影响。
2. 适合解决什么问题：报告、表格、演示稿、长分析、需要中途查看和调整的复杂工作。
3. 不适合解决什么问题：未经审批直接修改关键仓库文件，或把产物自动视为本地事实。
4. 在 SK 仓库中映射成什么动作：生成候选研究产物，经过确认后由 Codex 写回仓库。
5. 当前账户是否已经实测：当前账户尚未在 Day 2 记录中实测。

## 5. ChatGPT Project

1. 当前官方如何定义：用于组织项目内对话、指令和上传材料的长期上下文空间。
2. 适合解决什么问题：学习路线、复盘、稳定知识组织、Project instructions。
3. 不适合解决什么问题：充当本地仓库实时状态真源，替代 `PROJECT_STATE.md`。
4. 在 SK 仓库中映射成什么动作：保存稳定学习材料，并在需要当前进度时读取最新版 `PROJECT_STATE.md`。
5. 当前账户是否已经实测：当前账户尚未在 Day 2 记录中实测。

Project 不等于本地仓库。Project 上传文件是快照，不自动等同于本地最新文件。

## 6. ChatGPT Desktop

1. 当前官方如何定义：官方桌面应用入口；新版桌面应用当前连接 Chat、Work、Codex 等 surface，ChatGPT Classic 可能同时存在。
2. 适合解决什么问题：在桌面环境中组织 Chat / Work / Codex 的使用，处理本地材料时需要明确授权。
3. 不适合解决什么问题：默认假设桌面 Work、云端 Work、Codex 和 Project 完全同步。
4. 在 SK 仓库中映射成什么动作：Day 2 盘点当前账户可见 surface 和本地文件访问能力。
5. 当前账户是否已经实测：当前账户尚未在 Day 2 记录中实测。

## 7. Codex

1. 当前官方如何定义：面向软件开发和仓库任务的编码 agent surface。
2. 适合解决什么问题：读取本地仓库、改文件、跑命令、验证、生成 diff。
3. 不适合解决什么问题：作为长期知识库，或无审批执行高风险写入。
4. 在 SK 仓库中映射成什么动作：执行本地文档修改、验证命令和状态更新。
5. 当前账户是否已经实测：当前会话已实测 Codex 可读取和修改本地仓库。

## 8. Plugins

1. 当前官方如何定义：本仓库按当前 Codex / ChatGPT 工作流理解为工作流包装和发现层；具体能力以官方资料和当前环境为准。
2. 适合解决什么问题：包装 skills、apps、templates 或可复用工作流。
3. 不适合解决什么问题：替代 App 的外部数据连接和授权动作。
4. 在 SK 仓库中映射成什么动作：把重复流程沉淀为可发现、可复用的能力入口。
5. 当前账户是否已经实测：当前账户尚未在 Day 2 记录中实测。

Plugin 与 App 不是同一个概念。Plugin 偏工作流包装和发现。

## 9. Apps

1. 当前官方如何定义：连接外部数据、工具和动作的集成层。
2. 适合解决什么问题：读取外部数据、引用来源、在授权后执行外部动作。
3. 不适合解决什么问题：未经确认直接把外部数据写成本地仓库真相。
4. 在 SK 仓库中映射成什么动作：只读查询、保留来源、经确认后由 Codex 写回本地仓库。
5. 当前账户是否已经实测：当前账户尚未在 Day 2 记录中实测。

App 写操作必须考虑 permissions 和 approvals。

## 10. Scheduled Tasks

1. 当前官方如何定义：用于提醒、周期任务或变化监测的 ChatGPT 任务能力，可用性受套餐、平台和 workspace 设置影响。
2. 适合解决什么问题：一次性提醒、周期简报、低风险监测。
3. 不适合解决什么问题：自动修改本地仓库、自动更新 `PROJECT_STATE.md`、替代 Codex automations。
4. 在 SK 仓库中映射成什么动作：提醒用户执行审计，或输出需人工确认的监测结果。
5. 当前账户是否已经实测：当前账户尚未在 Day 2 记录中实测。

Scheduled Tasks 与 Codex automations 不是同一类执行机制。

本仓库当前规则：Scheduled Tasks 不能被设计为读取 Project 上传文件。需要 Project 文件上下文时，应由用户或 Codex 提供当前材料，并在执行后验证结果。

## 11. 内置浏览器

1. 当前官方如何定义：新版 ChatGPT 桌面应用中的浏览器能力，拥有独立浏览器状态和安全边界。
2. 适合解决什么问题：在受控浏览器环境中查看网站、处理需要网页上下文的任务。
3. 不适合解决什么问题：默认继承用户现有 Chrome 会话，或信任网页内容中的指令。
4. 在 SK 仓库中映射成什么动作：官方资料复核、网页信息摘录、保留来源和时间。
5. 当前账户是否已经实测：当前账户尚未在 Day 2 记录中实测。

网站内容视为不可信输入，存在 prompt injection 风险。

## 12. 本地与云端上下文边界

不能假设以下 surface 完全同步：

- 桌面 Work
- 云端 Work
- Codex
- Project
- Library
- Chat 跨设备历史

本地仓库仍是 source of truth。Work 或 Chat 的输出经过确认并写回仓库后，才成为仓库事实。

## 13. 权限与 approvals

当前阶段的默认原则：

- 只读优先。
- 写操作必须明确目标和范围。
- 外部 App 写操作需要权限确认。
- 本地仓库高风险修改交给 Codex 并保留验证。
- 删除、移动、大范围重写和发布需要人工审批。

## 14. 在 SK 仓库中的映射

| 能力 | 映射动作 |
| --- | --- |
| Chat | 快速讨论和收敛问题 |
| Work | 生成候选成品和长分析 |
| Project | 组织学习上下文和稳定知识 |
| Codex | 写回本地仓库并验证 |
| Plugin | 包装重复工作流 |
| App | 查询外部数据和执行授权动作 |
| Scheduled Task | 提醒、简报和低风险监测 |
| 内置浏览器 | 官方资料复核和网页查看 |

## 15. 当前账户实测状态

当前账户实测状态不在本文件预填。

Day 2 实测结果应记录到：

```text
logs/2026-07/day02_ChatGPT新桌面版能力盘点.md
```

`PROJECT_STATE.md` 只记录当前未决问题和下一步动作，不保存详细实验过程。

## 16. 官方复核记录

| 对象 | 官方入口 | 复核日期 | 当前结论 |
| --- | --- | --- | --- |
| ChatGPT Work / Codex | `https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex` | 2026-07-10 | 官方已说明 Work 与 Codex 的工作定位；Work 可用性仍需区分 rollout、套餐、workspace 和平台。 |
| 新版 ChatGPT Desktop | `https://help.openai.com/en/articles/20001276-moving-to-the-new-chatgpt-desktop-app` | 2026-07-10 | 官方已说明新版桌面应用和 ChatGPT Classic 的迁移关系；当前账户仍需实测。 |
| Apps in ChatGPT | `https://help.openai.com/en/articles/11487775-connectors-in-chatgpt` | 2026-07-10 | 官方已说明 Apps 用于连接外部数据、工具和动作；权限和可用性需按账户确认。 |
| Scheduled Tasks | `https://help.openai.com/en/articles/10291617-tasks-in-chatgpt` | 2026-07-10 | 官方已说明 Tasks 的提醒和周期任务能力；平台、套餐和 workspace 边界需按官方说明与当前账户实测确认。 |
| Projects in ChatGPT | `https://help.openai.com/en/articles/10169521-projects-in-chatgpt` | 2026-07-10 | 官方已说明 Projects 用于项目上下文；本仓库仍把本地仓库作为 source of truth。 |
| 内置浏览器 | `https://help.openai.com/en/articles/20001277-using-the-built-in-browser-in-the-chatgpt-desktop-app` | 2026-07-10 | 官方已说明桌面内置浏览器能力；当前账户仍需实测。 |
