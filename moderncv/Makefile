## Makefile per la compilazione del curriculum vitae (moderncv)

MAIN    := curriculum-vitae-moderncv
LATEX   := lualatex
LATEXFLAGS := -interaction=nonstopmode -halt-on-error

# estensioni generate dalla compilazione, da rimuovere con `make clean`
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
