# AGENTS.md

## 项目定位

本仓库是 **SK Agent OS 学习台**，用于系统学习个人 Agent 工作流设计。

Hermes 是机制样本，不是默认主力执行器。Codex / Claude Code 用于实际仓库执行，ChatGPT Project 用于学习、复盘和知识沉淀。

## 工作原则

1. 开始任务前先读 `README.md`，再读 `docs/00_项目定位.md`。
2. 不要把 Hermes 默认升级成主力生产工具。
3. 不要把高频变化状态写入长期知识文件。
4. 优先输出最小可运行版本。
5. 自动化默认只读，不自动写入、不自动删除、不自动提交。
6. 修改 Markdown 时保持正常多行格式，不要压成单行。
7. 涉及 OpenAI / Claude Code / Hermes 功能判断时，优先查官方资料，并更新 `docs/09_官方资料索引与复核清单.md` 的复核日期或过期风险。
8. ChatGPT Project 中的文件视为快照；本地仓库和 `PROJECT_STATE.md` 才是当前进度来源。
9. 涉及项目定位、学习计划、知识同步、当前阶段、当前进度或 `PROJECT_STATE.md` 本身时，修改前必须先读取 `PROJECT_STATE.md`。
10. 普通 typo、标点、纯格式修复，不要求强制读取 `PROJECT_STATE.md`。

## 目录说明

- `docs/`：稳定学习材料。
- `project/`：ChatGPT Project / GPTS 配置材料。
- `templates/`：可复用模板。
- `examples/`：已填好的最小样例。
- `logs/`：学习记录，不建议上传知识库。
- `archive/`：旧定位或废弃材料。

## 修改规则

1. 修改定位类文件时，必须同步检查 `README.md` 和 `docs/00_项目定位.md`。
2. 修改知识库清单时，必须同步检查 `project/Knowledge_Files_Checklist.md`。
3. 修改 ChatGPT Project 指令时，必须同步检查 `project/ChatGPT_Project_Setup.md`。
4. 新增模板时，必须说明适用场景、不适用场景、输入、输出、验收标准。
5. 新增样例时，必须能看出它如何从 `templates/` 中某个模板落地。
6. 不得加入 API key、token、私密仓库路径、实时外部状态。
7. `PROJECT_STATE.md` 可以记录当前进度，但不要把它当作长期知识文件。

## 验收

- Markdown 标题、列表、表格、代码块正常显示。
- `.gitignore` 每条规则独立成行。
- 新文件有清晰用途。
- 不把临时状态混入长期知识。
- 自动化样例默认只读，并写明写入升级条件。
- `git diff --check` 通过。
