.PHONY: all clean

TARGET=beamer.pdf

TEXENGINE=pdflatex
#TEXENGINE=xelatex --shell-escape

all: target $(addprefix target/,$(TARGET))

target/%.pdf: %.markdown preamble.tex
	pandoc -s -t beamer -H "preamble.tex" --base-header-level=1 \
		-o $(basename $@).tex $<
	latexmk -pdf -pdflatex="$(TEXENGINE) -halt-on-error -interaction=nonstopmode -file-line-error -synctex=1" \
		-output-directory='target' $(basename $@)

target:
	mkdir -p "./target"

clean:
	rm -rf target/
	rm -rf missfont.log
