#### Build environment #########################################################

TEX  = xelatex
BIB  = biber
SUPPORTED_LANG = en ru fa

#### Build entities ############################################################

BUILDDIR = build
TEX_SRC = book.tex
BIB_SRC = $(TEX_SRC:.tex=)

#### Build rules ###############################################################
first:
help:
%:
	@echo "Valid build targets:"
	@echo $(SUPPORTED_LANG)
	@echo "clean"
$(SUPPORTED_LANG): $(BUILDDIR)
	$(TEX) --output-directory=$(BUILDDIR) \
			'\providecommand{\lang}{$@}\input{$(TEX_SRC)}'
	$(BIB) --output-directory=$(BUILDDIR) $(BIB_SRC)
	$(TEX) --output-directory=$(BUILDDIR) \
			'\providecommand{\lang}{$@}\input{$(TEX_SRC)}'
	$(TEX) --output-directory=$(BUILDDIR) \
			'\providecommand{\lang}{$@}\input{$(TEX_SRC)}'
$(BUILDDIR):
	mkdir -p $(BUILDDIR)
clean:
	$(RM) -r $(BUILDDIR)
