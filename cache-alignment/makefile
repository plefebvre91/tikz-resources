all: poster-alignment.pdf

.PHONY: poster-alignment.pdf
poster-alignment.pdf: main.tex img/*.tex
	pdflatex main.tex
	sleep 1
	pdflatex main.tex

.PHONY: clean
clean:
	rm -f *.log *.aux *.snm *.nav *~ *.out *.toc *.vrb 2> /dev/null
