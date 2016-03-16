LaTeX-Boilerplate
=================

This is a personal template and boilerplate for writing *very-simple* scientific articles, with Markdown, Pandoc, and \LaTeX.

* [Article](article/article.markdown) [(Preview PDF)](https://github.com/wookayin/latex-boilerplate/blob/gh-pages/pdf/article.pdf)
* [Beamer](beamer/beamer.markdown)    [(Preview PDF)](https://github.com/wookayin/latex-boilerplate/blob/gh-pages/pdf/beamer.pdf)

It is of draft state; several improvements will be added later.


## Bootstrap Your Project

You can bootstrap your writing (article or beamer) in a single command, if you have `svn` installed.

```bash
# Article
svn export https://github.com/wookayin/latex-boilerplate/trunk/article your-article-name

# Beamer
svn export https://github.com/wookayin/latex-boilerplate/trunk/beamer your-beamer-name
```

Your new workspace directory (e.g. `./your-article-name`) will contain the same contents
as the current master of
[article/](https://github.com/wookayin/latex-boilerplate/tree/master/article) or
[beamer/](https://github.com/wookayin/latex-boilerplate/tree/master/beamer) directory.

Go get checkout, and start your writing with `git init`!
