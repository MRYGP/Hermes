# Hermes 关键概念速查

这份文档只记录第一阶段需要学的 Hermes 概念。目标是可迁移，不是覆盖全部功能。

## 当前定位说明

Hermes 当前作为 Agent OS 机制教材与对照实验台。

学习 Hermes 的目标不是用它替代 ChatGPT、Codex 或 Claude Code，而是理解 profile、memory、skills、cron、gateway、hooks、approvals、compression 等机制如何组合。

当前 ChatGPT 产品能力与 Hermes 机制的阶段性对照，见 [docs/10_ChatGPT_工作台能力地图.md](10_ChatGPT_工作台能力地图.md)。

## profile

profile 是一个 agent 的隔离空间。

它通常包含：

- config
- API keys
- memory
- sessions
- skills
- gateway state

在 SK 里的用途：

> 把“SK 仓库维护 agent”和其他项目 agent 隔离，避免记忆、工具、任务状态串线。

第一阶段只需要理解 profile 的边界，不急着做复杂分发。

## memory

memory 用来保存长期稳定事实，不适合保存短期状态。

适合记：

- 用户长期偏好
- 项目长期目标
- 稳定术语定义
- 不常变化的协作规则

不适合记：

- 当前工单状态
- 本周扫描结果
- 临时实验结论
- 高频变动的发布进度

在 SK 里的用途：

> 只记录长期有效的项目原则，不记录实时看板。

## skills

skill 是可复用流程。

适合做成 skill 的动作：

- 状态漂移审计
- 发布包生成
- 收尾联动检查
- 项目复盘
- 文档结构检查

在 SK 里的用途：

> 把“每次都要解释一遍的流程”固化为可调用能力。

## quick commands

quick command 适合零推理或低推理的机械动作。

适合：

- 打开固定文件
- 生成固定格式摘要
- 执行固定检查
- 输出固定模板

不适合：

- 需要复杂判断的任务
- 有高风险写入的任务

在 SK 里的用途：

> 把常用维护动作变成固定入口，减少每次重新描述。

## AGENTS.md

AGENTS.md 是项目级规则文件。

适合写：

- 项目边界
- 文件组织
- 修改规则
- 验证命令
- 不要做什么

不适合写：

- 大量背景长文
- 频繁变化的任务状态
- 临时灵感

在 SK 里的用途：

> 让 Codex / Claude Code / 其他 agent 进入仓库后先知道基本规则。

## cron / automations

cron 或 automations 用于周期性任务。

适合：

- 每日状态漂移审计
- 每周知识库过期检查
- 定期雷达扫描
- 发布前检查

不适合：

- 未验证过的写入流程
- 需要大量人工判断的任务

在 SK 里的用途：

> 先从“只读审计”开始，不要一开始自动改仓库。

## hooks / approvals

hooks 和 approvals 是安全边界。

适合拦截：

- 删除文件
- 大范围移动
- 写入关键文档
- 修改配置
- 运行高风险命令

在 SK 里的用途：

> 让 agent 可以自动做低风险动作，但高风险动作必须停下来确认。

## compression

compression 是上下文压缩策略。

适合：

- 长会话后保留关键状态
- 把过程压缩成决策记录
- 降低后续 token 成本

不适合：

- 压缩后丢失验收标准
- 把不稳定信息写成长期事实

在 SK 里的用途：

> 把阶段性过程压缩成“当前事实 + 未决问题 + 下一步动作”。
