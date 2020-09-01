fileinfo := LaTeX Makefile for Poster 
author := Miguel Xochicale
version := alpha1

## Tools
LATEXMK = latexmk
RM = rm -f
EVINCE = evince

##Project name
PROJNAME=main

## Rules
$(PROJNAME).pdf: $(PROJNAME).tex
	$(LATEXMK) -pdf -pdflatex="pdflatex -shell-escape -synctex=1 -file-line-error %O %S" $<

view:
	$(EVINCE) $(PROJNAME).pdf

mostlyclean:
	$(LATEXMK) -silent -C

clean: mostlyclean
	$(LATEXMK) -silent -c
	$(RM) main.pdf *.bbl *.run.xml
