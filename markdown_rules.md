# Markdown Rules for Quantum-Mechanics-Notes

Purpose
- Provide clear, consistent markdown conventions for contributors to this repository.
- Ensure notes are readable, reproducible, and easy to convert to notebooks/slides.

1. Scope
- This file covers file naming, front matter, headings, math, code blocks, figures, citations, PR checklist, and CI suggestions.

2. File & folder naming
- Use lowercase, hyphen-separated filenames: `topic-name.md`, `section-name.md`.
- Place topical notes under `/notes/<topic-folder>/` (e.g., `/notes/quantum-foundations/`).
- Use `README.md` in folders to describe folder purpose.

3. Front matter / Metadata (recommended)
- Optional but encouraged. Include at top of file as plain text block:

```
Title: Short descriptive title
Authors: Name1, Name2
Date: YYYY-MM-DD
Tags: [tag1, tag2]
Status: draft  # draft | review | final
```

4. Headings & structure
- One H1 per file: the file's main topic (# Title).
- H2 for major sections (Theory, Examples, Exercises, References).
- H3/H4 for subsections; avoid deeper nesting if possible.
- Keep sections short and self-contained.

5. Math and notation
- Inline math: `$...$` for short expressions.
- Display math: `$$...$$` for equations on their own line.
- Define symbols at first use and maintain a short symbol table for long notes.
- Prefer standard notation and document any local conventions.

6. Code blocks & notebooks
- Use fenced code blocks with language tag:

```bash
mkdir -p ~/quantum-notes && cd ~/quantum-notes
git clone https://github.com/CriticalLine/Quantum-Mechanics-Notes
```

- For reproducible examples, put executable notebooks in `/notebooks/` and link from notes.
- Keep examples minimal and include expected output or quick checks.

7. Figures, diagrams & assets
- Store images under `/assets/<topic>/` and reference relatively: `![Caption](../assets/quantum/fig1.png)`.
- Preferred formats: SVG for diagrams, PNG for raster images.
- Include captions and short alt text for accessibility.

8. Citations & references
- Use a `References` section with numbered entries.
- For papers/books include full citation and a DOI or URL where possible.

9. Cross-references & anchors
- Use explicit anchors for long documents when linking to figures/equations.
- Prefer relative links for repo portability.

10. Examples & templates
- Provide a minimal note template and a derivation template in this file's appendix.

Minimal note template:

```
# Title

Authors: ...
Date: YYYY-MM-DD

## Overview

Short 1–2 sentence summary.

## Main Content

Step-by-step derivation or explanation.

## Example

## Conclusions

## References
```

11. Commit & PR conventions
- Branch from `main` using `feature/<short-desc>` or `edit/<file-name>`.
- Keep commits atomic; reference section or issue in the commit message.
- PR checklist (enforced by reviewers):
  - [ ] File name follows convention
  - [ ] Has Title, Authors, Status
  - [ ] Math renders correctly
  - [ ] Figures stored under /assets
  - [ ] References present for non-original content
  - [ ] Status: draft/review/final set

12. Review & attribution
- Add a short reviewer note at top when requesting review.
- Credit external sources inline and in References.

13. CI / automation suggestions
- Run `markdownlint` or similar to enforce basic style.
- Optionally run a LaTeX/math render check.
- For notebooks: run a lightweight execution test on new/changed notebooks.

14. Appendix: common commands
- Clone repo example:

```bash
mkdir -p ~/project/quantum-notes && cd ~/project/quantum-notes
git clone https://github.com/CriticalLine/Quantum-Mechanics-Notes
```

- Create branch & commit example:

```bash
git checkout -b edit/markdown-rules
git add quantum-notes/markdown_rules.md
git commit -m "docs: add markdown rules and templates"
git push --set-upstream origin edit/markdown-rules
```

---

Contributors: add suggestions as PRs to `edit/markdown-rules`.
