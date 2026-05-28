# Translation Rules

## Style

- Use clear Simplified Chinese academic prose.
- Prefer faithful translation over rhetorical rewriting.
- Keep the author's claims, uncertainty, limitations, and causal language intact.
- Avoid adding explanations that are not in the source unless clearly labeled as translator notes.
- Do not summarize when the user asked for full translation.

## Terminology

- Create and maintain a terminology table before translating long papers.
- Keep one Chinese translation for each key term after it is chosen.
- For first occurrences of important terms, use Chinese plus English in parentheses.
- Preserve established English names for algorithms, datasets, software, benchmarks, and institutions when Chinese translation would reduce clarity.

Examples:

| English | Preferred Chinese |
|---|---|
| robust optimization | 鲁棒优化 |
| two-stage robust optimization | 两阶段鲁棒优化 |
| column-and-constraint generation | 列与约束生成 |
| Benders decomposition | Benders 分解 |
| recourse | 追索 |
| uncertainty set | 不确定集 |
| mixed-integer programming | 混合整数规划 |

## Symbols, variables, and formulas

- Do not translate mathematical variables, indices, set names, or equation labels.
- Keep displayed equations and inline formulas in LaTeX format whenever possible.
- Preserve equation numbers and cross-references such as `(3)`, `Eq. (3)`, `constraint (7b)`.
- If PDF extraction corrupts mathematical symbols, reconstruct the formula in LaTeX from the rendered PDF when feasible; otherwise keep a translator note and point to the source page/equation number.
- Translate explanatory phrases around formulas.
- Do not replace mathematical notation with prose summaries.

## Citations and references

- Keep in-text citations intact: `(Zeng and Zhao, 2013)`, `[12]`, `Zeng & Zhao [3]`.
- Do not translate author names in reference entries.
- Do not translate paper titles inside the reference list unless the user explicitly requests a Chinese bibliography.
- Preserve DOI, journal names, volume, issue, pages, and URLs.

## Abstract and keywords

- Translate the abstract as a polished Chinese academic abstract.
- Preserve technical specificity and quantitative claims.
- Translate keywords, but keep abbreviations and proper nouns when needed.

## Tables and captions

- Translate table headers, notes, and captions.
- Keep numeric values, units, confidence intervals, and statistical notation unchanged.
- Preserve figure/table numbering exactly.

## Translator notes

Use short notes only when necessary:

- source text is unreadable or likely OCR-corrupted;
- a formula, figure, or table cannot be extracted reliably;
- an English term has no stable Chinese equivalent and needs user confirmation.
