# Quality Checklist

Use this checklist before delivering a translated paper.

## Completeness

- Title, authors, abstract, keywords, all sections, references, and appendices are present.
- No source section is skipped.
- No figure, table, displayed equation, caption, footnote, or important note is missing.
- All cross-references still point to the correct figure/table/equation/section numbers.
- The default final deliverable is a complete Markdown translation saved next to the source paper.

## Translation fidelity

- Claims, assumptions, limitations, and conclusions match the source.
- Technical terms are consistent across the document.
- Variables, symbols, model names, dataset names, and algorithm names are preserved.
- Citations remain intact and are not translated incorrectly.
- No major English paragraph remains untranslated unless intentionally preserved.

## Academic Chinese quality

- Sentences are readable Chinese, not mechanical word-for-word English order.
- Abstract and conclusion sound like Chinese academic writing.
- Long sentences are split only when meaning is preserved.
- Hedging words such as "may", "can", "suggest", "approximately", and "under certain conditions" are preserved.

## Layout fidelity

- Markdown headings, captions, tables, and figures are readable.
- Figures and tables appear near the related translated discussion.
- Figures and tables are placed at their corresponding source locations rather than grouped at the end, unless the user requested an appendix.
- Figure/table image links point to cropped visual regions plus captions whenever possible, not whole-page screenshots.
- Any whole-page screenshot fallback is explicitly noted with the reason cropping was not reliable.
- Equations are not corrupted.
- Markdown image links resolve.
- DOCX visual checks are performed only when the user explicitly requests DOCX or publication-like layout.

## Delivery note

When delivering, state:

- output files created;
- any pages/figures/tables that could not be extracted cleanly;
- whether the result is full Markdown translation, bilingual comparison, or Markdown note;
- whether figure/table cropping was completed or any whole-page screenshot fallback was used;
- whether optional DOCX visual verification was completed, if DOCX was requested.
