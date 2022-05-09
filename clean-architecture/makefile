all: main.pdf

PLANTUML_BIN=$(HOME)/plantuml-1.2022.5.jar
PLANTFILES_DIR=plant-files
IMG_DIR=img

.PHONY: main.pdf
main.pdf: generate-plant-svg convert-images main.tex
	pdflatex main.tex
	sleep 1
	pdflatex main.tex

generate-plant-svg:
	java -jar $(PLANTUML_BIN) -tsvg $(PLANTFILES_DIR)

convert-images:
	inkscape --export-area-drawing $(PLANTFILES_DIR)/srp-good.svg         --export-pdf=$(IMG_DIR)/srp-good.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/srp-bad.svg          --export-pdf=$(IMG_DIR)/srp-bad.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/srp-good-facade.svg  --export-pdf=$(IMG_DIR)/srp-good-facade.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/ocp-general.svg      --export-pdf=$(IMG_DIR)/ocp-general.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/lsp-good.svg         --export-pdf=$(IMG_DIR)/lsp-good.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/isp-good.svg         --export-pdf=$(IMG_DIR)/isp-good.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/isp-bad.svg          --export-pdf=$(IMG_DIR)/isp-bad.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/dip-good.svg         --export-pdf=$(IMG_DIR)/dip-good.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/dip-bad.svg          --export-pdf=$(IMG_DIR)/dip-bad.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/services.svg          --export-pdf=$(IMG_DIR)/services.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/package-layer.svg     --export-pdf=$(IMG_DIR)/package-layer.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/package-feature.svg   --export-pdf=$(IMG_DIR)/package-feature.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/package-domain.svg    --export-pdf=$(IMG_DIR)/package-domain.pdf
	inkscape --export-area-drawing $(PLANTFILES_DIR)/package-component.svg --export-pdf=$(IMG_DIR)/package-component.pdf
	rm $(PLANTFILES_DIR)/*.svg

.PHONY: clean
clean:
	rm -f *.bcf *.xml *.log *.aux *.snm *.nav *~ *.out *.toc *.vrb $(IMG_DIR)/*.pdf $(PLANTFILES_DIR)/*.svg 2> /dev/null
