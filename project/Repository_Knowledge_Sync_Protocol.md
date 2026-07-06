# Repository Knowledge Sync Protocol

## 核心原则

本地仓库是 source of truth。ChatGPT Project 中的文件是某个时间点的快照，不会自动等同于本地最新仓库。

因此：

- 稳定知识可以上传到 ChatGPT Project。
- 当前进度以 `PROJECT_STATE.md` 为准。
- 高频变化内容留在本地仓库，不作为长期知识上传。
- Project 如果缺少最新状态，必须要求用户上传或粘贴最新文件，而不是凭旧聊天推断。

## Project 每次开始时应检查

1. 是否能看到最新 `PROJECT_STATE.md`。
2. `PROJECT_STATE.md` 是否与用户当前问题一致。
3. 相关 docs / project / templates 文件是否被上传。
4. 是否存在超过 30 天未复核的外部工具判断。
5. 用户是否要求执行本地仓库修改；如果是，应交给 Codex，而不是只在 Project 中空谈。

## 同步频率

### 每次结构性修改后

更新：

- `README.md`
- `PROJECT_STATE.md`
- `project/Knowledge_Files_Checklist.md`

### 每次 ChatGPT Project 知识库更新前

检查：

- 是否包含临时状态。
- 是否包含过期外部结论。
- 是否包含不应上传的 logs / archive。

### 每 30 天

复核：

- `docs/09_官方资料索引与复核清单.md`
- Codex / Claude Code / Hermes / ChatGPT Project 的关键功能判断。

## 上传策略

### 长期知识包

上传稳定文件：

- 项目定位
- 学习地图
- 工具分工
- 概念速查
- 实战映射
- 规则边界
- 排错与省 token
- 模板

### 当前状态包

按需上传或粘贴：

- `PROJECT_STATE.md`
- 当前正在讨论的具体文件
- 最近一次修改摘要

当前状态包不等于长期知识库。它用于让 Project 理解进度。

## Project 不能做的假设

- 不能假设本地仓库已经和 Project 上传文件同步。
- 不能把旧聊天中的状态当作当前事实。
- 不能把 `logs/` 的学习记录当作稳定规则。
- 不能把官方工具功能判断永久化。

## 给 Project 的标准开场检查

```text
请先检查你是否有最新 PROJECT_STATE.md。
如果没有，请要求我上传或粘贴最新 PROJECT_STATE.md。
然后再基于仓库中的稳定知识文件回答，不要使用旧聊天状态作为当前事实。
```
