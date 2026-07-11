# Knowledge Files Checklist

这份清单用于决定哪些文件适合上传到 ChatGPT Project 或未来 GPTS 知识库。

## A. Project instructions

```text
project/ChatGPT_Project_Instructions.md
```

处理方式：

> 复制到 Project settings，不作为普通知识文件重复上传。

## B. 长期稳定知识

这些文件用于长期理解项目。

```text
docs/00_项目定位.md
docs/01_Agent_OS_学习地图.md
docs/02_工具分工对照表.md
docs/03_Hermes_关键概念速查.md
docs/04_SK_仓库实战映射.md
docs/05_自动化优先级清单.md
docs/07_记忆技能规则边界.md
docs/08_排错与省Token手册.md
project/Repository_Knowledge_Sync_Protocol.md
```

## C. 阶段性、需替换知识

这些文件可以上传，但产品能力变化或阶段结束后需要替换，不能视为永久稳定知识。

```text
docs/06_7到14天学习计划.md
docs/09_官方资料索引与复核清单.md
docs/10_ChatGPT_工作台能力地图.md
templates/chatgpt_capability_experiment_template.md
```

## D. 当前状态包

```text
PROJECT_STATE.md
当前正在讨论的具体文件
最近一次结构修改摘要
```

当前状态包不等于长期知识库。它用于让 Project 理解进度。

## 明确排除

```text
logs/
archive/
每日 git 输出
未验证实验结果
旧版 PROJECT_STATE.md
临时研究材料
```

## 判断规则

可以上传：

> 长期有效、稳定、可复用、不会频繁变动。

不应上传：

> 当前状态、临时判断、易过期信息、需要频繁同步的内容。

## 上传前检查

上传前问 5 个问题：

1. 这个文件 30 天后还大概率有效吗？
2. 它是规则、概念、流程，还是当前状态？
3. 它是否包含过期风险很高的信息？
4. 它是否会让 GPT 把旧状态当真？
5. 它是否应该留在本地仓库，由 Codex 读取，而不是放进知识库？
