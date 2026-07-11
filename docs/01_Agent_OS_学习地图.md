# Agent OS 学习地图

## Agent OS 是什么

这里的 Agent OS 不是操作系统软件，而是一套个人 AI 代理的组织方式。

它回答的问题是：

```text
一个 AI agent 如何长期理解我、理解项目、执行固定流程、避免越界、降低成本，并在多个工具之间保持稳定协作？
```

## 核心结构

| 层级 | 负责什么 | 常见载体 |
| --- | --- | --- |
| 身份层 | agent 是谁，默认风格是什么 | profile、project instructions、system prompt |
| 记忆层 | 长期事实、偏好、稳定背景 | memory、知识库、项目文档 |
| 规则层 | 项目约束、执行边界、验证方式 | AGENTS.md、CLAUDE.md、仓库规范 |
| 技能层 | 可复用流程 | skills、slash commands、quick commands |
| 工具层 | 读写文件、调用 API、跑命令 | MCP、shell、Apps、gateway |
| 调度层 | 定时任务、周期审计、后台检查 | cron、automations、Scheduled Tasks |
| 安全层 | 审批、hook、sandbox、权限边界 | approvals、hooks、sandbox、permissions |
| 成本层 | 上下文压缩、模型选择、文件裁剪 | compression、prompt-size、fallback model |

## 稳定学习顺序

1. 先理解 project instructions / AGENTS.md：固定边界。
2. 再理解 skills / quick commands：固定动作。
3. 再理解 memory / knowledge：固定事实。
4. 再理解 approvals / hooks：固定安全线。
5. 再理解 cron / gateway / automations：固定调度。
6. 最后理解 compression / fallback：固定成本。

## 当前 v2 学习路径

当前产品实践线：

```text
Chat / Work / Project / Codex
-> Plugins / Apps
-> Scheduled Tasks
-> 权限、审批和上下文同步
```

机制理解线：

```text
memory
-> skills
-> AGENTS.md
-> approvals / hooks
-> automation / cron
-> compression
```

落地线：

```text
把以上能力映射到 SK 仓库中的真实动作。
```

产品 surface 会变。Agent OS 的结构问题相对稳定。

## Hermes 在这张图里的位置

Hermes 的价值在于它把很多 Agent OS 机制放在一起：profile、memory、skills、cron、gateway、hooks、MCP、compression、provider 策略等。

所以 Hermes 适合作为机制教材与对照实验台。

但具体干活时，Codex 和 Claude Code 通常更适合作为执行器。

## 学完后应该获得什么

学完这个仓库，不要求你成为 Hermes 专家。真正目标是获得以下判断力：

- 哪些事实应该进入 memory。
- 哪些流程应该做成 skill。
- 哪些机械动作应该做成 quick command。
- 哪些规则应该写进 AGENTS.md。
- 哪些任务适合自动化。
- 哪些自动化现在不值得做。
- 哪些操作必须加审批或 hook。
- 哪些内容不应该进入长期知识库。
