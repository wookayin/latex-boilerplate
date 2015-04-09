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
- Nested List Level 1
    - Nested List Level 2
        - Nested List Level 3
- Mathematical notations
$$
e^{i \pi} + 1 = 0
$$
- `Verbatim` texts and Code blocks (see Section \ref{highlighted-codes})
- Images and Pictures (TODO)
- Bibilographies (TODO)


\newpage

## Highlighted Codes, powered by `minted`
\label{highlighted-codes}

One can insert syntax-highlighted codes into the document, thanks to `minted` package.
The build process would require `Pygments` python package;
make sure that the `pygmentize` is available from the command-line.
The document-wide global option is specified in `preamble.tex`, and a listing can override options as well.

\bigskip
OK, now let's see in action --- here is a sample C++ snippet:

\begin{minted}[mathescape,frame=single]{cpp}
/* A C++ Code that computes $\mathrm{gcd}(x, y)$ in $O(\log n)$ time */
auto gcd(int x, int y) -> int {
    return y == 0 ? x : gcd(y, x % y);
}
\end{minted}

Or, even an inline code: do you see the \mintinline{cpp}{auto} part?

**Note**: If you are going to insert lots of code snippets, or separate out code contents into external files, then `minted`'s shortcut feature (e.g.
\mintinline{latex}{\pythoninline/print True/} or \mintinline{latex}{\inputpython{demo.py}}, etc.) might be useful. However, to my knowledge, there is an issue of unwanted escapings with pandoc, so demonstrations of these are omitted as of now.




\newpage

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
- [minted.sty Documentation](https://github.com/gpoore/minted)
- [User-contributed Templates](https://github.com/jgm/pandoc/wiki/User-contributed-templates)
- [jgm/pandoc-templates](https://github.com/jgm/pandoc-templates)



<!------------------------------------------------------------------------>
\newpage

# Lorem Ipsum

## Subsection: Lorem Ipsum

\lipsum[1]

### Subsubsection: Lorem Ipsum

\lipsum[2-4]
