mdfiles := $(wildcard *.md)
pdffiles := $(mdfiles:.md=.pdf)

all : $(pdffiles)


%pdf : %.md
	pandoc --standalone --mathjax -V header-includes="\\usepackage[all]{xy}" -V include-before="\\input macros.tex" $< -o $@



