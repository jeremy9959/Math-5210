mdfiles := $(wildcard *.md)
pdffiles := $(mdfiles:.md=.pdf)

all : $(pdffiles)


%.pdf : %.md
	pandoc --standalone --mathjax -V include-before="\\input macros.tex" $< -o $@

