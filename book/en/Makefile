TEX  = xelatex

BUILDDIR = build

all:
	mkdir -p $(BUILDDIR)
	$(TEX) --output-directory=$(BUILDDIR) book.tex
	$(TEX) --output-directory=$(BUILDDIR) book.tex

clean:
	rm -rf $(BUILDDIR)
