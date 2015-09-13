.PHONY: all clean

TARGET=beamer.pdf

all: target $(addprefix target/,$(TARGET))

target/%.pdf: %.markdown preamble.tex
	pandoc -s -t beamer -H "preamble.tex" --base-header-level=1 \
		-o $(basename $@).tex $<
	latexmk -pdf -pdflatex="xelatex --shell-escape -halt-on-error -interaction=nonstopmode" \
		-output-directory='target' $(basename $@)

target:
	mkdir -p "./target"

clean:
	rm -rf target/
