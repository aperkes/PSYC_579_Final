.PHONY: all
all: final.pdf

sections: $(shell find sections -type f)

figures: $(shell find figures -type f)

final.pdf: final.bbl final.aux
	pdflatex ./final.tex
	pdflatex ./final.tex

final.dat: final.tex sections figures
	pdflatex ./final.tex

final.bbl: final.dat
	bibtex final.aux

.PHONY: clean
clean:
	rm -f *aux *bbl *blg *idx *log *dat

.PHONY: realclean
realclean: clean
	rm -f final.pdf
