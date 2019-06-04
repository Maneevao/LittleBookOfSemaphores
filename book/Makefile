TEX  = xelatex

BUILDDIR = build

en: $(BUILDDIR)
	$(TEX) --output-directory=$(BUILDDIR) '\providecommand{\lang}{en}\input{book.tex}'
	$(TEX) --output-directory=$(BUILDDIR) '\providecommand{\lang}{en}\input{book.tex}'
ru: $(BUILDDIR)
	$(TEX) --output-directory=$(BUILDDIR) '\providecommand{\lang}{ru}\input{book.tex}'
	$(TEX) --output-directory=$(BUILDDIR) '\providecommand{\lang}{ru}\input{book.tex}'

$(BUILDDIR):
	mkdir -p $(BUILDDIR)

clean:
	$(RM) -r $(BUILDDIR)
