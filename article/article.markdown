---
title: A Personal \LaTeX + Markdown Writing Template
author: Jongwook Choi
date: \today

fontsize: 10pt
geometry: top=1in, bottom=1in, left=1in, right=1in
numbersections: true
graphics: true
---


# About

This is a personal template and boilerplate
for writing *very-simple* scientific articles, based on Markdown and \LaTeX.

# Features and Demonstrations

- A separate directory for build (`/target`)
- 한글 및 漢字가 포함된 문서 작성
    - \textbf{굵게}, \textit{이탤릭체}, \texttt{타이프라이터}, \textsf{세리프}
    - \textbf{Bold}, \textit{Italic}, \texttt{Typewriter}, \textsf{Serif}
    - 글꼴 변경: 나눔명조 및 은바탕
- Mathematical notations
$$
e^{i \pi} + 1 = 0
$$
- Images and Pictures
- `Verbatim` texts and Code blocks
- Bibilographies

# Technical Details

## Tools (tested on Mac OS X)

- [Pandoc](http://johnmacfarlane.net/pandoc/) for converting markdown sources into \LaTeX files.
  (Tested with 1.13.2)
- [\XeLaTeX](http://www.xelatex.org/) for typesetting into PDF.
  (Tested with Tex Live 2013)

## Structures

- `Makefile` (see TARGET)
- `document-title.markdown` : The raw source in Markdown
- `premable.tex` : The premable for settings styles, etc.
- `target/document-title.pdf` : The deliverable.
- `images/` : A collection of images embedded in the document.

# References

- [Pandoc's Markdown](http://johnmacfarlane.net/pandoc/README.html#pandocs-markdown)
- [\XeTeX-ko 간단 매뉴얼](http://mirror.hmc.edu/ctan/macros/xetex/generic/xetexko/xetexko-doc.pdf)
- [User-contributed Templates](https://github.com/jgm/pandoc/wiki/User-contributed-templates)
- [jgm/pandoc-templates](https://github.com/jgm/pandoc-templates)



<!------------------------------------------------------------------------>
\newpage

# Lorem Ipsum

## Subsection: Lorem Ipsum

\lipsum[1]

### Subsubsection: Lorem Ipsum

\lipsum[2-4]
