FILES = presentation.pdf presentation.html

FILTERS = --citeproc --filter pandoc-crossref
PDF_ENGINE = --pdf-engine=lualatex
PDF_OPTIONS = -t beamer --number-sections
REVEALJS_THEME = beige

all: $(FILES)

%.pdf: %.md
	pandoc "$<" $(FILTERS) $(PDF_ENGINE) $(PDF_OPTIONS) -o "$@"

%.html: %.md
	pandoc "$<" --embed-resources --standalone -t revealjs -V theme=$(REVEALJS_THEME) -o "$@"

clean:
	rm -f $(FILES)
