FILENAME=gandouin-leclercq-roupin_roadef18

all: $(FILENAME).pdf

$(FILENAME).pdf: $(wildcard *.tex *.bib fig/*) 
	pdflatex $(FILENAME).tex || true
	bibtex $(FILENAME) || true
	pdflatex $(FILENAME).tex || true
	pdflatex $(FILENAME).tex

clean:
	rm -f *.dvi *.log *.aux *.bbl *.blg *~ $(FILENAME).pdf
