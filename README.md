# Real Analysis

> Measure-theoretic real analysis lecture notes and 12 weeks of fully worked homework, bilingual (Chinese/English), following Zhang Xicheng's lecture notes and Folland's *Real Analysis*.

The notes follow **《实变函数论》 (Real Analysis) lecture notes by Zhang Xicheng (张希承)** (104 pp., included in `textbooks/`) with **Folland, *Real Analysis: Modern Techniques and Their Applications*, 2nd ed.** as the second reference. Entry numbering uses the book-style three-part scheme (e.g. **Theorem 1.2.9**).

## Repository structure

```
real-analysis/
├── cn/
│   ├── notes.md              # Chinese lecture notes (single file, 964 lines)
│   └── homework/
│       └── week1.md … week12.md
├── en/
│   ├── notes.md              # Complete English translation (964 lines, aligned)
│   └── homework/
│       └── week1.md … week12.md
└── textbooks/
    ├── real-analysis.pdf             # Zhang Xicheng's lecture notes (104 pp.)
    ├── real-analysis_ocr.pdf
    ├── folland.pdf                   # Folland, 2nd ed. (402 pp.)
    └── folland_ocr.pdf
```

## The notes

`notes.md` is the longest of the pure-mathematics note repositories — **964 lines, 99 entries, 11 chapters**:

1. Sets and preliminaries
2. Algebraic and measurable structure
3. Measures and measurable sets
4. Lebesgue measure and regularity
5. Measurable functions
6. The Lebesgue integral and convergence theorems
7. Convergence of sequences of functions
8. Product measures and multiple integrals
9. Signed measures and the Radon–Nikodym theorem
10. Bounded variation and absolute continuity
11. Appendix: background facts

Both the Chinese and English versions are line-for-line aligned (964 lines each), so they can be read side by side.

## The homework

Each `homework/weekN.md` follows the series-wide format:

1. **Toolbox** — a blockquote restating the definitions and theorems needed for the week;
2. **Problems** — the assigned exercises;
3. **Solutions** — complete worked proofs ending with `$\blacksquare$`.

There are **12 weeks** of problem sets, the shortest semester in the series.

## Bilingual layout

- `cn/` — authoritative Chinese version.
- `en/` — complete parallel English translation with identical structure.

## The `textbooks/` folder

The PDFs are **external reference material** (the lecture notes and Folland's textbook, plus OCR copies for searchability), not documents compiled from the notes. There is no build system; everything is plain Markdown rendered with GitHub's LaTeX support.

## Related repositories

Other course-notes repositories in the same series: [abstract-algebra](https://github.com/wenje-ma/abstract-algebra), [advenced-algebra](https://github.com/wenje-ma/advenced-algebra), [topology](https://github.com/wenje-ma/topology), and the full list on the [profile page](https://github.com/wenje-ma).
