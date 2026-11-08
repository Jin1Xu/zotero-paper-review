# Zotero Paper Review

用于查证和解读论文的 Codex Skill。提供论文标题、DOI、链接或 Zotero 条目，即可生成带来源链接的中文解读，并更新已有的 Zotero 条目。

## 安装

```bash
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/Jin1Xu/zotero-paper-review.git "$HOME/.agents/skills/zotero-paper-review"
```

使用 Zotero 写入功能需要 Zotero Desktop、Codex 的 Zotero 插件和桌面操作权限。完整写入还要求 Zotero 提供「标题翻译」「简记」「摘要翻译」字段。[Codex Skill 安装文档](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)

## 使用

在 Codex 对话中输入以下任一指令。

```text
$zotero-paper-review 论文标题或 DOI
$zotero-paper-review 论文标题或 DOI，只解读
```

第一条会更新唯一匹配的已有 Zotero 条目。第二条会把解读返回到对话中。存在多个匹配时，请选定条目。添加新条目需明确提出导入。

## 写入内容

- 补全**条目信息**，包括英文原标题、标题翻译、短标题、简记、摘要翻译和日期。
- 保存带原始来源链接的**子笔记**，涵盖文献信息、关键词、模型与训练、数据集和局限性。
- 将关键词写入「**#标签**」。有原文关键词时照录，否则提炼 4–5 个。按情况补充开源状态和文章类型标签。

完整工作流程见 [SKILL.md](SKILL.md)。
