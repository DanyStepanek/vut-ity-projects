PROJ=proj1
PACK=xharmi00-fit

.PHONY: clean pack

$(PROJ).pdf: $(PROJ).ps
	ps2pdf $(PROJ).ps

$(PROJ).ps: $(PROJ).dvi
	dvips $(PROJ).dvi

$(PROJ).dvi: $(PROJ).tex
	latex $(PROJ).tex

$(PACK).tar.gz: $(PROJ).tex
	tar -czf $(PACK).tar.gz Makefile $(PROJ).tex

pack: $(PACK).tar.gz

clean:
	rm -f $(PROJ).aux $(PROJ).dvi $(PROJ).log $(PROJ).ps
