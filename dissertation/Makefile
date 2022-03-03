# This Makefile defines the rules for building the dissertation PDF from the
# LaTeX sources.
#
# Usage:
#
#   "make" or "make build": Generate "dissertation.pdf".
#   "make clean": Remove any generated files, including the PDF.
#   "make show": Generate and open the PDF in a browser.
#
###############################################################################

# The name of the main .tex file to build.
DOCUMENT = dissertation.tex

# The name of the PDF that should be produced
PDF = $(patsubst %.tex,%.pdf,$(DOCUMENT))

# List other files that are needed for building the PDF
TEX_FILES := $(filter-out $(DOCUMENT), $(wildcard *.tex))
BIB_FILES := $(wildcard *.bib)
FIGURES := $(wildcard figures/*)

# Rules for building, showing, and cleaning
all: $(PDF)

$(PDF): $(DOCUMENT) $(TEX_FILES) $(BIB_FILES) $(FIGURES)
	tectonic -X compile $<

show: $(PDF)
	python -c "import webbrowser; webbrowser.open('$<')" &

clean:
	rm -rvf $(PDF) figures/*eps-converted-to.pdf
