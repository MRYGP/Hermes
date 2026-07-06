# Knowledge Files Checklist

这份清单用于决定哪些文件适合上传到 ChatGPT Project 或未来 GPTS 知识库。

## 推荐上传

第一批推荐上传：

- `docs/00_项目定位.md`
- `docs/01_Agent_OS_学习地图.md`
- `docs/02_工具分工对照表.md`
- `docs/03_Hermes_关键概念速查.md`
- `docs/04_SK_仓库实战映射.md`
- `docs/07_记忆技能规则边界.md`
- `docs/08_排错与省Token手册.md`
- `templates/skill_template.md`
- `templates/quick_command_template.md`
- `templates/automation_audit_template.md`

## 暂不推荐上传

暂不推荐长期上传：

- 高频变化的项目看板。
- 每日任务状态。
- 每周扫描结果。
- 临时实验记录。
- 未确认的外部信息。
- 近期发布状态。

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
