# xhs-note

小红书/XHS 笔记批量生成 skill。

## 功能

- 读取包含笔记标题与正文的 Excel、CSV、XLSX 或 TSV 表格。
- 筛选正文超过 200 字的笔记。
- 提炼标题模板、内容模板和选题方向。
- 联网搜索素材，倒序套用模板生成新标题与新正文。
- 输出筛选表、模板表和最终原文/生成内容对比 Excel。

## 文件

- `SKILL.md`：skill 主说明与执行流程。
- `agents/openai.yaml`：Codex/OpenAI agent 展示配置。

## 示例文件

示例目录：[examples/xhs_note_ai_invest_20260521_1420](examples/xhs_note_ai_invest_20260521_1420)

这组示例展示了一次完整的 XHS 笔记批量处理流程，从原始输入表到最终对比表：

- [input_ai_invest_20260521_1420.xlsx](examples/xhs_note_ai_invest_20260521_1420/input_ai_invest_20260521_1420.xlsx)：原始输入表，包含小红书笔记 ID、链接、标题、正文、话题、点赞量、收藏量等字段。
- [filtered_notes_over_200_chars.xlsx](examples/xhs_note_ai_invest_20260521_1420/filtered_notes_over_200_chars.xlsx)：筛选结果表，只保留正文字符数严格大于 200 的笔记，并保留原文行号、原标题、原文内容和原文字数。
- [xhs_note_template_list.xlsx](examples/xhs_note_ai_invest_20260521_1420/xhs_note_template_list.xlsx)：模板表，记录每条筛选后笔记抽象出的选题方向、内容类型、标题模板、内容结构、模板说明和变量清单。
- [all_notes_original_vs_generated_reverse_templates.xlsx](examples/xhs_note_ai_invest_20260521_1420/all_notes_original_vs_generated_reverse_templates.xlsx)：最终对比表，按倒序模板生成新标题和新正文，并逐行保留原文、使用模板行号、参考来源、拓展素材摘要、改写差异说明和备注。
