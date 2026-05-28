# Layout Preservation

## General principle

Preserve the reader's ability to map the Chinese document back to the original paper. Keep section order, numbering, figures, tables, formulas, captions, appendices, and references aligned with the source.

## PDF source workflow

1. Render or inspect representative pages before extraction.
2. Detect whether the paper is single-column, two-column, or mixed layout.
3. Extract text in reading order; if extraction order is wrong, repair it manually section by section.
4. Extract images and record page number, figure number, and caption.
5. Crop visual material to the figure/table region plus its caption whenever possible; avoid whole-page screenshots by default.
6. Preserve page-critical visual material even when OCR text extraction is incomplete, but state any fallback clearly.

## Figures and images

- Keep every original figure unless the user explicitly says otherwise.
- Preserve figure numbers and translate captions.
- Crop figures to the visual region plus the original caption area whenever possible.
- Place each figure near the corresponding translated paragraph, matching the source paper's local flow; do not move figures to an end appendix unless the user requests that.
- If producing Markdown, place images in a sibling folder and link with stable relative paths.
- If producing DOCX, insert figures near the translated paragraph where they originally appear.
- Do not redraw figures unless the user requests a translated/redesigned version.
- If a figure contains important embedded English labels, either keep it and translate the caption, or add a short translated explanation below it.
- Use a whole-page render only when the figure boundary cannot be identified reliably; note the fallback in the delivery note.

## Tables

- Recreate simple tables as editable tables in DOCX/Markdown.
- For complex tables that would lose structure, preserve a cropped image containing only the table body and its caption, then translate the caption/notes.
- Keep numeric values, units, symbols, significance stars, and confidence intervals unchanged.
- Preserve table numbers and cross-references.
- Place each table near the corresponding translated paragraph or section where the source paper places/discusses it; do not collect tables in an appendix by default.
- Do not preserve an entire page just to keep a table unless table-only cropping fails or would cut off rows, columns, notes, or the caption.

## Equations

- Preserve displayed equations visually or as editable LaTeX equation text when reliable.
- In Markdown, use `$...$` for inline formulas and `$$...$$` for displayed equations.
- In DOCX, prefer editable equation objects or clear LaTeX text when equation-object conversion would corrupt symbols.
- Keep equation numbers and cross-references.
- Translate surrounding prose, variable definitions, assumptions, and explanations.
- Do not alter symbols, domains, constraints, objective functions, or index notation.

## DOCX formatting

- Use heading styles for title, abstract, section headings, subsections, references, and appendices.
- Keep captions close to their figures/tables.
- Use page breaks sparingly; prioritize readable layout over exact page-by-page reproduction unless the user asks for strict facsimile.
- Render the DOCX to images/PDF for visual QA when layout fidelity matters.

## Markdown formatting

- Use Obsidian-friendly Markdown.
- Preserve heading hierarchy with `#`, `##`, and `###`.
- Use LaTeX delimiters for equations where appropriate.
- Use Markdown tables only when they remain readable; otherwise link table images.
- Store images in a local folder such as `images/` and use stable names like `fig-01.png`, `table-02.png`.
- Prefer image links to cropped figures/tables plus captions, not full rendered PDF pages.
- Keep image links in the translated section where the original figure/table belongs, not in a consolidated appendix.

## What not to do

- Do not drop figures, tables, formulas, captions, or appendices for convenience.
- Do not use whole-page screenshots as the normal way to preserve figures or tables.
- Do not silently reorder sections.
- Do not translate references into prose summaries.
- Do not replace mathematical notation with an informal verbal description unless the user asks for an explanatory note.
