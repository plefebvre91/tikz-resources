all: main.pdf

.PHONY: main.pdf
main.pdf: main.tex
	pdflatex main.tex

.PHONY: clean
clean:
	rm -f *.bcf *.xml *.log *.aux *.snm *.nav *~ *.out *.toc *.vrb 2> /dev/null
