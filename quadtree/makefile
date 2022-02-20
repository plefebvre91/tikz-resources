all: poster-quadtree.pdf

.PHONY: poster-quadtree.pdf
poster-quadtree.pdf: main.tex img/*.tex
	pdflatex main.tex
	sleep 1
	pdflatex main.tex

.PHONY: clean
clean:
	rm -f *.log *.aux *.snm *.nav *~ *.out *.toc *.vrb 2> /dev/null
