.PHONY: all clean

TARGET=article.pdf

all: target $(addprefix target/,$(TARGET))

target/%.pdf: %.markdown preamble.tex
	pandoc -s -t latex -H "preamble.tex" --base-header-level=1 \
		-o $(basename $@).tex $<
	xelatex --shell-escape -halt-on-error -interaction=nonstopmode \
		-output-directory='target' $(basename $@).tex

target:
	mkdir -p "./target"

clean:
	rm -rf target/ *.pyg
