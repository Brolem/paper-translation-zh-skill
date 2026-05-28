---
name: paper-translation-zh
description: Translate English academic papers into faithful Chinese scholarly documents while preserving paper structure, figures, tables, formulas, captions, numbering, references, and layout. Use when Codex is asked to translate or localize English papers, PDF/DOCX manuscripts, arXiv papers, journal articles, conference papers, theses, or technical reports into Chinese; create Chinese DOCX and Markdown outputs; produce bilingual comparison drafts; keep images, equations, tables, section hierarchy, citations, and academic formatting intact; or review Chinese translations of academic papers for terminology, omissions, and layout fidelity.
---

# Paper Translation ZH

## Purpose

Translate English academic papers into Chinese with fidelity to both meaning and document structure. Default to a faithful Chinese scholarly draft, not a free paraphrase, and deliver both DOCX and Markdown unless the user requests another format.

Use existing file-format skills when needed:

- Use `pdf` for PDF reading, page rendering, image extraction, layout inspection, and page-level verification.
- Use `documents:documents` for DOCX creation, editing, comments, redlines, and render-and-verify workflows.
- Use plain Markdown for Obsidian-ready reading notes or lightweight translated manuscripts.

## Workflow

1. **Inventory the source**
   - Identify file type, page count, title, authors, abstract, section hierarchy, references, appendix, figures, tables, and equations.
   - If the source is a PDF, inspect visual pages before assuming text order. Multi-column papers often need layout-aware extraction.
   - Build a short layout map: section titles, figure/table numbers, equation numbers, and pages with important visual elements.

2. **Lock output mode**
   - Default: Chinese DOCX + Chinese Markdown.
   - Use bilingual output only when requested or when the user needs close proofreading.
   - Preserve paper-level structure: title, abstract, keywords, numbered sections, subsections, captions, acknowledgments, references, and appendices.

3. **Create a terminology table**
   - Keep technical terms consistent across the paper.
   - Preserve variable names, mathematical symbols, dataset names, algorithm names, model names, and citation keys.
   - On first occurrence of important terms, use Chinese with English in parentheses when helpful, such as `列与约束生成（column-and-constraint generation, C&CG）`.

4. **Translate section by section**
   - Translate faithfully first; polish only enough to produce natural Chinese academic prose.
   - Do not omit hedging, assumptions, limitations, negative results, or experimental conditions.
   - Keep paragraph order unless layout extraction is clearly wrong.
   - Mark uncertain or corrupted source text with a concise translator note instead of silently guessing.

5. **Preserve figures, tables, equations, and layout**
   - Keep all original images unless the user explicitly asks to remove or redraw them.
   - Keep figure/table numbers and captions aligned with the translated discussion.
   - Preserve displayed equations, inline formulas, and equation numbers in LaTeX whenever possible; translate surrounding explanatory text, not symbols.
   - Recreate tables with translated headers/cells where practical; otherwise preserve the table image and add a translated caption or nearby note.
   - Follow `references/layout-preservation.md` for detailed handling.

6. **Generate deliverables**
   - DOCX: use document tooling and visually verify rendered pages when layout matters.
   - Markdown: use Obsidian-friendly headings, image links, equations, tables, and citation text.
   - Save extracted images in a sibling image folder when producing Markdown, using stable names such as `fig-01.png`.
   - For long papers, use the part-by-part workflow in `references/batch-translation.md` before attempting a merged final version.

7. **Quality check before delivery**
   - Read `references/quality-checklist.md`.
   - Check for missing sections, missing figures/tables, broken numbering, broken equations, inconsistent terms, untranslated English fragments, and references accidentally translated.

## Reference Files

Load only the reference needed for the task:

- `references/translation-rules.md`: academic Chinese style, terminology, variables, abbreviations, citations, LaTeX formulas, and references.
- `references/layout-preservation.md`: preserving figures, tables, LaTeX formulas, captions, numbering, DOCX layout, and Markdown image handling.
- `references/batch-translation.md`: split long papers into Part1, Part2, Part3, and a merged final version while preserving section boundaries.
- `references/quality-checklist.md`: final acceptance checklist for translation fidelity and layout fidelity.

## Defaults

- Output language: Simplified Chinese.
- Translation style: faithful academic Chinese.
- Deliverables: DOCX + Markdown.
- Keep original paper assets: yes.
- Keep references in original bibliographic form: yes, unless the user asks for a citation-style conversion.
- Do not use external translation APIs by default. Translation is performed by Codex/model reasoning under this workflow.
