# Batch Translation Workflow

Use this workflow for long academic papers that cannot be translated reliably in one pass.

## Default split

Create three part files and one merged Markdown file in the source paper's directory:

1. `*_中文翻译_Part1.md`
   - Title, authors, abstract, keywords, introduction, and literature review.
   - Usually covers Sections 1-2.
2. `*_中文翻译_Part2.md`
   - Mathematical model, reformulation, decomposition method, algorithms, and main methodology.
   - Usually covers Sections 3-4 or the technical core.
3. `*_中文翻译_Part3.md`
   - Learning enhancements, computational experiments, conclusion, references notes, appendices, and supplements.
   - Usually covers the remaining sections.
4. `*_中文翻译.md`
   - Merge Part1, Part2, and Part3 after all part files are complete.
   - This merged Markdown file is the default final deliverable.

## Splitting rules

- Split by section boundaries, not by arbitrary page counts.
- Keep equations, figures, tables, captions, and references with the section that discusses them.
- For figures and complex tables, keep cropped figure/table images plus captions with the section that discusses them.
- If a section is very long, split at subsection boundaries and note the continuation clearly.
- Do not create a merged final file until all part files are complete.

## File header

Each part file should start with:

```markdown
# 中文翻译 Part N

- 原文文件: ...
- 覆盖范围: ...
- 翻译状态: 完整 / 待续 / 需人工复核
- 说明: ...
```

## Merge rules

- Preserve the original section order.
- Remove duplicate terminology tables unless the user wants them retained.
- Keep a single quality note at the top of the merged file.
- Verify that figure/table/equation numbering is still monotonic and cross-references remain readable.
- Verify that visual links point to cropped figure/table images rather than whole-page screenshots, unless a fallback note explains why cropping was not reliable.

## Progress reporting

When the paper is too long for one turn, complete the next part file rather than pretending the entire translation is done. In the final response, state which part is complete and which Markdown files remain.
