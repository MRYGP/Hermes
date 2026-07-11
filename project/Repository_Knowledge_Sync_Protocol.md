# Repository Knowledge Sync Protocol

## 路径规则

真实路径是：

```text
project/Repository_Knowledge_Sync_Protocol.md
```

禁止在仓库根目录新建第二份：

```text
Repository_Knowledge_Sync_Protocol.md
```

## 核心原则

本地仓库是 source of truth。ChatGPT Project 中的文件是某个时间点的快照，不会自动等同于本地最新仓库。

ChatGPT 新能力不会改变 source of truth 原则。

即使 Work 或 Codex 可以读取本地文件，本地仓库仍然是 source of truth。

即使 Project 可以连接外部 Apps，外部数据也不会自动替代 `PROJECT_STATE.md`。

即使 Chat 可以跨设备同步，也不能假设桌面 Work、云端 Work、Codex 和 Project 共享完全相同的上下文。

## 上下文优先级

1. 本地仓库最新文件。
2. 最新 `PROJECT_STATE.md`。
3. 用户本轮明确提供的具体材料。
4. Project 中的稳定知识快照。
5. 当前会话中已经确认的信息。
6. 旧聊天记录。

## Project 每次开始时应检查

1. 是否能看到最新 `PROJECT_STATE.md`。
2. `PROJECT_STATE.md` 是否与用户当前问题一致。
3. 相关 docs / project / templates 文件是否被上传。
4. 是否存在超过 30 天未复核的外部工具判断。
5. 用户是否要求执行本地仓库修改；如果是，应交给 Codex，而不是只在 Project 中空谈。

## 知识更新流程

1. 修改本地仓库。
2. 运行验证。
3. 更新 `PROJECT_STATE.md`。
4. 按知识清单替换 Project 文件。
5. 更新 Project instructions。
6. 上传最新版 `PROJECT_STATE.md`。
7. 开新会话测试状态识别。

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
- 是否包含不应上传的 `logs/` / `archive/`。

### 每 30 天

复核：

- `docs/09_官方资料索引与复核清单.md`
- Codex / Claude Code / Hermes / ChatGPT Project 的关键功能判断。

## 上传策略

### 长期稳定知识

上传稳定文件：

- 项目定位
- 学习地图
- 工具分工
- 概念速查
- 实战映射
- 自动化原则
- 规则边界
- 排错与省 token
- 同步协议

### 阶段性、需替换知识

按阶段上传：

- 学习计划
- 官方资料索引
- 当前能力地图
- 当前阶段实验模板

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
- 不能把 Work 产物、Task 输出或 App 数据直接当成仓库事实。

## 给 Project 的标准开场检查

```text
请先检查你是否有最新 PROJECT_STATE.md。
如果没有，请要求我上传或粘贴最新 PROJECT_STATE.md。
然后再基于仓库中的稳定知识文件回答，不要使用旧聊天状态作为当前事实。
```
