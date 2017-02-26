PROJ=proj1

.PHONY: clean

$(PROJ).pdf: $(PROJ).ps
	ps2pdf $(PROJ).ps

$(PROJ).ps: $(PROJ).dvi
	dvips $(PROJ).dvi

$(PROJ).dvi: $(PROJ).tex
	latex $(PROJ).tex

clean:
	rm -f $(PROJ).aux $(PROJ).dvi $(PROJ).log $(PROJ).ps
