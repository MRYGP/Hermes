# Day 01：为什么现在还要学 Hermes

日期：2026-07-06

## 1. 当前为什么不把 Hermes 当主力执行器

我现在不把 Hermes 当主力执行器，原因不是 Hermes 没价值，而是主力执行层已经有更合适的工具。

当前我的仓库工作需要的是稳定读文件、改文件、生成 patch、验证修改、维护文档结构。这个层面，Codex 和 Claude Code 更直接，也更适合承担实际执行。它们已经覆盖了大部分“让 agent 在仓库里干活”的需求。

所以，如果目标只是维护 SK 仓库、修改文档、整理项目状态、生成配置和模板，我不应该先绕到 Hermes 里做一套执行系统。那会把学习工具变成建设工具本身，增加复杂度，也容易让我重新陷入“为了自动化而自动化”。

当前口径应该固定为：

```text
Codex / Claude Code 负责当下干活。
Hermes 负责理解 Agent OS 如何组织。
ChatGPT Project 负责学习、复盘和沉淀。
```

## 2. 为什么仍然值得学 Hermes

Hermes 仍然值得学，是因为它把个人 Agent 系统里很多关键机制放在一起，适合作为 Agent OS 的样本。

我要学的不是“怎样多一个代码助手”，而是：

- 一个 agent 如何隔离项目身份。
- 一个 agent 如何管理长期记忆。
- 一个 agent 如何把重复流程沉淀为技能。
- 一个 agent 如何区分机械动作和推理任务。
- 一个 agent 如何做周期性任务。
- 一个 agent 如何设置审批、hook 和安全边界。
- 一个 agent 如何控制上下文长度和 token 成本。

这些能力即使最后不在 Hermes 里生产使用，也能迁移到 Codex、Claude Code、ChatGPT Project 和未来的 SK 工作流里。

因此，Hermes 对我当前的价值是教材价值，不是执行器价值。

## 3. Hermes 里最值得迁移到 SK 的机制

当前最值得迁移到 SK 的机制不是 gateway 或常驻代理，而是更基础的几层。

### profile：项目隔离

SK 需要明确项目边界，避免不同项目的记忆、术语、状态混在一起。

迁移方式：

- 用 ChatGPT Project 做学习上下文隔离。
- 用仓库级 `AGENTS.md` 做 Codex 进入项目后的规则入口。
- 未来为真实 SK 仓库单独设计自己的项目规则。

### memory：长期事实边界

SK 不能把每日状态、临时判断、过期结论写进长期记忆。

迁移方式：

- 长期原则进入稳定 docs。
- 当前进度进入 `PROJECT_STATE.md`。
- 学习过程进入 `logs/`，但不上传为长期知识库。

### skills：流程沉淀

SK 里真正值得沉淀的是重复执行的流程，而不是一次性任务。

优先候选：

- 状态漂移审计。
- 收尾联动检查。
- 发布包生成。
- 知识库过期检查。

### quick commands：机械动作入口

高频、低判断、固定格式的动作可以做成 quick command。

优先候选：

- 生成当前状态简报。
- 输出每日复盘模板。
- 列出知识库上传检查项。

### approvals / hooks：安全边界

SK 后续如果要自动化，必须先设计不能自动做什么。

优先规则：

- 默认只读。
- 不自动删除。
- 不自动重写长文。
- 不自动提交。
- 高风险修改必须人工确认。

### compression：会话收束

SK 项目长期推进时，最容易浪费 token 的地方是反复解释背景。

迁移方式：

- 每阶段压缩成当前事实、已完成、未决问题、下一步。
- 不把过程性长聊天当作长期知识。

## 4. 当前工具分工

| 工具 | 当前分工 |
| --- | --- |
| Codex | 本地仓库执行层，负责读文件、改文件、生成 diff、跑检查、维护结构。 |
| Claude Code | 复杂代码理解、大范围重构、工程型协作的补充执行层。 |
| Hermes | Agent OS 机制教材，用来学习 profile、memory、skills、cron、gateway、hooks、approvals、compression。 |
| ChatGPT Project | 学习、复盘、路线设计和知识沉淀中心。 |
| SK 仓库 | 最终落地场景，不在当前阶段急着自动化。 |

这个分工的核心是：执行归执行，学习归学习，状态归状态。

我不应该把 ChatGPT Project 当本地执行器，也不应该把 Hermes 当当前主力生产工具。Project 如果需要理解当前进度，必须看最新 `PROJECT_STATE.md`；Codex 如果需要执行修改，必须读本地仓库文件。

## 5. 下一步只做什么，不做什么

### 下一步只做

执行第 2 天任务：

```text
理解 AGENTS.md 与项目规则的边界，
起草一个真实 SK 仓库专用 AGENTS.md 大纲，
并标记哪些内容不能写入 AGENTS.md。
```

### 当前不做

- 不继续扩展仓库目录。
- 不急着做 GPTS。
- 不先研究 gateway 或常驻 agent。
- 不给真实 SK 仓库直接上自动化。
- 不把 `logs/` 上传为长期知识库。
- 不把 Hermes 重新定义为主力执行器。

## 6. 今日结论

我现在还要学 Hermes，但只轻学、结构化学、迁移式学。

我的目标不是掌握 Hermes 的所有功能，而是借 Hermes 看清一个个人 Agent OS 应该如何组织：

```text
固定脑子：profile / project instructions
固定事实：memory / knowledge
固定规则：AGENTS.md
固定动作：skills / quick commands
固定边界：approvals / hooks
固定节奏：cron / automations
固定成本：compression / prompt-size
```

只要这些判断能迁移回 Codex、Claude Code、ChatGPT Project 和 SK 仓库，Hermes 的学习就是值得的。
