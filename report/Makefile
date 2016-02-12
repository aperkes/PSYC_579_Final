.PHONY: all
all: final.pdf

sections: $(shell find sections -type f)

figures: $(shell find figures -type f)

final.pdf: sections figures final.tex
	pdflatex ./final.tex
	pdflatex ./final.tex

.PHONY: clean
clean:
	rm -f *aux *bbl *blg *idx *log *dat

.PHONY: realclean
realclean: clean
	rm -f final.pdf
