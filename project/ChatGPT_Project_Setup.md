# ChatGPT Project Setup

> `project/ChatGPT_Project_Instructions.md` 是 Project instructions 的唯一维护源。
>
> 本文件只负责说明如何创建 Project、配置 memory、复制 instructions、上传知识文件、上传当前状态和做配置验收。

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

## 知识文件上传

按 `project/Knowledge_Files_Checklist.md` 执行。

优先上传长期稳定知识。阶段性、需替换知识可以上传，但产品能力变化或阶段结束后需要替换。

不要上传 `logs/`、`archive/`、每日 git 输出、临时研究材料或未验证实验结果。

## 当前状态同步

第一次创建 Project 时，额外上传或粘贴一次 `PROJECT_STATE.md`，让 Project 获得当前进度。

之后每次结构性修改后，都应上传最新版 `PROJECT_STATE.md` 或粘贴其关键内容。

`PROJECT_STATE.md` 是当前状态入口，不属于长期稳定知识库。

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

## 配置验收问题

配置完成后，开一个新会话测试：

```text
请先检查是否有最新版 PROJECT_STATE.md。

然后回答：

1. 本仓库的长期定位是什么。
2. 当前 v2 阶段优先学习什么。
3. “ChatGPT 工作台”是否为官方产品名称。
4. Hermes 当前承担什么角色。
5. 当前状态以哪个文件为准。
6. 现在最值得做的一个动作是什么。
```
