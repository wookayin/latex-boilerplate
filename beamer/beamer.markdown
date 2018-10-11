---
fontsize: 10pt
classoption:
  - t
  - aspectratio=43

title: A Simple Beamer Presentation
author: Jongwook Choi
date: \today
---

Introduction
============

## About

Beamer is awesome!

\pause
Ta-da!

## List

* Item Level 1
    * Item Level 2
        * Item Level 3


## Math

Mathematical expressions are shown in Roman style as
$$
p(\theta \mid D) = \frac{
  p(D \mid \theta) \cdot p(\theta)
}{
  p(D)
}
$$
rather than the (default) serif style.


## Blocks

You can use three pre-defined blocks and other beamer blocks(e.g. \texttt{theorem}) as well.

\begin{block}{Default}
  Block with \texttt{\textbackslash begin\{block\}}.
\end{block}

\begin{alertblock}{Alert}
  Block with \texttt{\textbackslash begin\{alertblock\}}.
\end{alertblock}

\begin{exampleblock}{Example}
  Block with \texttt{\textbackslash begin\{exampleblock\}}.
\end{exampleblock}


## Themes and Other Links

- List of available beamer themes \cite{ReferenceA}.
- Beamer User Guide \cite{BeamerGuide}.


## References {.allowframebreaks}

\small

\bibliographystyle{plain}
\begin{thebibliography}{9}
    \bibitem{ReferenceA} LaTeX Beamer Themes. \url{http://latex.simon04.net/}
    \bibitem{BeamerGuide} The \textsf{beamer} class: User Guide. \url{http://texdoc.net/texmf-dist/doc/latex/beamer/doc/beameruserguide.pdf}
\end{thebibliography}


Thank You!
==========
