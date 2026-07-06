# ChatGPT Project Setup

> Project Instructions 的唯一维护源是 `project/ChatGPT_Project_Instructions.md`。本文件只负责说明 Project 怎么创建、上传哪些文件、创建后怎么同步状态。

## 项目名称

推荐：

```text
SK Agent OS 学习台
```

## Project Instructions

Project Instructions 字段使用 `project/ChatGPT_Project_Instructions.md` 的完整内容。

不要在本文件里维护第二份指令正文，避免两个版本漂移。

## Memory 设置

如果创建界面提供记忆范围选择，优先选择：

```text
Project-only memory
```

原因：这个项目需要隔离 SK Agent OS 学习上下文，避免与其他项目、普通聊天或无关仓库状态互相污染。

## 第一批上传文件

按 `project/Knowledge_Files_Checklist.md` 执行。优先上传稳定知识，不上传 `logs/` 和 `archive/`。

第一次创建 Project 时，额外上传或粘贴一次 `PROJECT_STATE.md`，让 Project 获得当前进度。之后它仍然只作为当前状态入口，不作为长期知识库文件。

## 每次使用前的推荐提问

```text
请先基于我上传的 PROJECT_STATE.md 判断当前阶段，然后告诉我现在最值得做的一个动作。
```

## Project 与 Codex 的交接方式

Project 负责：

- 判断路线。
- 拆解任务。
- 生成学习计划。
- 生成模板草案。
- 判断哪些文件适合进入知识库。

Codex 负责：

- 在本地仓库执行修改。
- 检查文件结构。
- 跑验证命令。
- 更新 `PROJECT_STATE.md`。
- 生成可提交的 diff。

## 创建后检查

Project 创建完成后，回到本地仓库更新 `PROJECT_STATE.md`：

```text
当前阶段：Project 已创建，进入第 1 天学习任务。
已完成：Project instructions 已配置；第一批稳定知识已上传；PROJECT_STATE.md 已同步。
下一步：执行 docs/06 第 1 天任务。
```
