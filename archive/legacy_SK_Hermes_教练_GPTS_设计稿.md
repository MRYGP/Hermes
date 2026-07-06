# SK × Hermes 教练 GPTS 设计稿

这个文件已完成 v2 修订，项目定位从 **SK Hermes 教练** 升级为 **SK Agent OS 学习台**。

修订后的正式设计稿见：

- [../project/SK_Agent_OS_学习台_GPTS_设计稿.md](../project/SK_Agent_OS_学习台_GPTS_设计稿.md)

## 修订要点

原定位：

```text
SK Hermes 教练
= 边学 Hermes，边把 SK 仓库用 Hermes 维护和更新
```

新定位：

```text
SK Agent OS 学习台
= 以 Hermes 为主教材
+ 以 Codex / Claude Code 为现实对照组
+ 以 SK 仓库为落地场景
+ 以 ChatGPT Project 为学习与复盘中心
```

## 为什么改名

Codex 和 Claude Code 已经覆盖了大量仓库执行能力，因此 Hermes 不再适合作为默认主力执行器。

Hermes 当前更适合作为 Agent OS 机制样本，用来学习：

- profile 隔离
- memory 边界
- skills 沉淀
- quick commands
- cron / gateway
- hooks / approvals
- compression / token cost

## 当前建议

先做 ChatGPT Project，不急着做 GPTS。

等 7-14 天学习和实践跑顺后，再把稳定材料封装成 GPTS。
