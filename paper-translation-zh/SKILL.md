---
name: paper-translation-zh
description: Translate English academic papers into faithful Chinese Markdown manuscripts while preserving paper structure, figures, tables, formulas, captions, numbering, references, and layout. Use when Codex is asked to translate or localize English papers, PDF/DOCX manuscripts, arXiv papers, journal articles, conference papers, theses, or technical reports into Chinese; create full Chinese Markdown translations; produce bilingual comparison drafts when requested; keep images, cropped figure/table regions with captions, equations, section hierarchy, citations, and academic formatting intact; or review Chinese translations of academic papers for terminology, omissions, and layout fidelity.
---

# Paper Translation ZH

## Purpose

Translate English academic papers into Chinese with fidelity to both meaning and document structure. Default to a complete Chinese Markdown manuscript, not a summary or free paraphrase. Generate DOCX only when the user explicitly requests it.

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
   - Default: Chinese Markdown saved next to the source file as `*_中文翻译.md`.
   - Generate DOCX only when the user explicitly requests Word/DOCX output.
   - Use bilingual output only when requested or when the user needs close proofreading.
   - Preserve paper-level structure: title, abstract, keywords, numbered sections, subsections, captions, acknowledgments, references, and appendices.

3. **Create a terminology table**
   - Keep technical terms consistent across the paper.
   - Preserve variable names, mathematical symbols, dataset names, algorithm names, model names, and citation keys.
   - On first occurrence of important terms, use Chinese with English in parentheses when helpful, such as `列与约束生成（column-and-constraint generation, C&CG）`.

4. **Translate section by section**
   - Translate the full paper paragraph by paragraph; do not substitute summaries for full translation.
   - Translate faithfully first; polish only enough to produce natural Chinese academic prose.
   - Do not omit hedging, assumptions, limitations, negative results, or experimental conditions.
   - Keep paragraph order unless layout extraction is clearly wrong.
   - Mark uncertain or corrupted source text with a concise translator note instead of silently guessing.

5. **Preserve figures, tables, equations, and layout**
   - Keep all original images unless the user explicitly asks to remove or redraw them.
   - Keep figure/table numbers and captions aligned with the translated discussion.
   - Place each preserved figure or table at the corresponding source location in the translated Markdown, near the paragraph that introduces or discusses it; do not collect figures/tables in an appendix by default.
   - Preserve displayed equations, inline formulas, and equation numbers in LaTeX whenever possible; translate surrounding explanatory text, not symbols.
   - For figures and complex tables, crop and preserve only the figure/table region plus its caption whenever possible; do not preserve a whole page screenshot by default.
   - Recreate simple tables with translated headers/cells where practical; otherwise preserve a cropped table image and add a translated caption or nearby note.
   - Use a whole-page screenshot only when reliable figure/table cropping is not possible, and state that limitation in the delivery note.
   - Follow `references/layout-preservation.md` for detailed handling.

6. **Generate deliverables**
   - Markdown: use Obsidian-friendly headings, image links, equations, tables, and citation text.
   - Save the default final file as `*_中文翻译.md` in the source paper's directory.
   - DOCX: only when requested, use document tooling and visually verify rendered pages when layout matters.
   - Save extracted images in a sibling image folder when producing Markdown, using stable names such as `fig-01.png`.
   - For long papers, use the part-by-part workflow in `references/batch-translation.md` before producing the merged Markdown version.

7. **Quality check before delivery**
   - Read `references/quality-checklist.md`.
   - Check for missing sections, missing figures/tables, broken numbering, broken equations, inconsistent terms, untranslated English fragments, and references accidentally translated.

## Reference Files

Load only the reference needed for the task:

- `references/translation-rules.md`: full academic Chinese translation style, terminology, variables, abbreviations, citations, LaTeX formulas, and references.
- `references/layout-preservation.md`: preserving cropped figures/tables with captions, LaTeX formulas, captions, numbering, optional DOCX layout, and Markdown image handling.
- `references/batch-translation.md`: split long papers into Part1, Part2, Part3, and a merged final version while preserving section boundaries.
- `references/quality-checklist.md`: final acceptance checklist for translation fidelity and layout fidelity.

## Defaults

- Output language: Simplified Chinese.
- Translation style: faithful academic Chinese.
- Deliverables: Markdown by default; DOCX only on explicit request.
- Keep original paper assets: yes.
- Keep references in original bibliographic form: yes, unless the user asks for a citation-style conversion.
- Do not use external translation APIs by default. Translation is performed by Codex/model reasoning under this workflow.
