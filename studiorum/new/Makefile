## Makefile per la compilazione del curriculum vitae et studiorum

MAIN    := cv-studiorum
LATEX   := pdflatex
LATEXFLAGS := -interaction=nonstopmode -halt-on-error

AUX_EXT := aux log out toc nav snm bbl blg synctex.gz

.PHONY: all pdf clean distclean view

all: pdf

pdf: $(MAIN).pdf

$(MAIN).pdf: $(MAIN).tex
	$(LATEX) $(LATEXFLAGS) $(MAIN).tex
	$(LATEX) $(LATEXFLAGS) $(MAIN).tex

view: pdf
	xdg-open $(MAIN).pdf >/dev/null 2>&1 &

clean:
	$(RM) $(foreach ext,$(AUX_EXT),$(MAIN).$(ext))

distclean: clean
	$(RM) $(MAIN).pdf
