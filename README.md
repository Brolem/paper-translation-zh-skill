# Paper Translation ZH

`paper-translation-zh` is a Codex skill for translating English academic papers into faithful Simplified Chinese Markdown manuscripts.

It is designed for papers, arXiv preprints, journal articles, conference papers, theses, and technical reports where structure and layout matter.

## Features

- Translate full English papers into Chinese paragraph by paragraph.
- Preserve the original paper structure: title, abstract, keywords, sections, subsections, acknowledgments, references, and appendices.
- Keep formulas in LaTeX whenever possible.
- Preserve figures and complex tables as cropped images containing the visual object plus its caption.
- Place translated figures and tables near their corresponding source locations, not in a final appendix by default.
- Preserve citation markers, variables, symbols, dataset names, model names, and bibliographic references.
- Default output is Markdown saved next to the source paper as `*_中文翻译.md`.
- Generate DOCX only when explicitly requested.

## Usage

Example prompt:

```text
Use $paper-translation-zh to translate this English paper into a faithful Chinese Markdown manuscript while preserving figures, cropped figure/table regions with captions, formulas, tables, and layout.
```

Typical Chinese prompt:

```text
[$paper-translation-zh] 帮我把这篇英文论文完整翻译成中文，保存在同级目录下，保留公式、图片、表格和原文结构。
```

## Output Rules

- Default deliverable: Markdown only.
- Default filename: `*_中文翻译.md`.
- Images: stored in a sibling image folder and linked from Markdown.
- Figures/tables: crop the figure or table region plus caption; avoid whole-page screenshots.
- Tables: recreate simple tables as Markdown only when structure is reliable; otherwise preserve cropped table images.
- References: keep original English bibliographic entries unless the user asks for a translated bibliography.

## Skill Structure

```text
paper-translation-zh/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── batch-translation.md
    ├── layout-preservation.md
    ├── quality-checklist.md
    └── translation-rules.md
```

## Installation

Copy the `paper-translation-zh` folder into your Codex skills directory:

```text
C:\Users\<YourUser>\.codex\skills\paper-translation-zh
```

Restart Codex after installation so the skill can be discovered.

## Notes

- This skill does not call external translation APIs by default.
- It relies on Codex/model reasoning plus available PDF and document tooling.
- For long papers, it uses a Part1 -> Part2 -> Part3 -> merged Markdown workflow.
