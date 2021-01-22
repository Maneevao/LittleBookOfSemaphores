#### Build configuration #######################################################

TEX = xelatex
TEX_SRC = book.tex
TEX_FLAGS = '\providecommand{\lang}{$@}\input{$(TEX_SRC)}' -halt-on-error

BIB = biber
BIB_SRC = $(TEX_SRC:.tex=)
BIB_FLAGS =

BUILD_DIR = build
COMMON_FLAGS = --output-directory=$(BUILD_DIR)/$@

#### Build rules ###############################################################

%:
	@echo "Valid build targets:"
	@echo $(SUPPORTED_LANG)
	@echo "clean"

SUPPORTED_LANG = en ru fa
ru:
en:
fa:
$(SUPPORTED_LANG):
	mkdir -p $(BUILD_DIR)/$@
	$(TEX) $(COMMON_FLAGS) $(TEX_FLAGS) $(TEX_SRC)
	$(BIB) $(COMMON_FLAGS) $(BIB_FLAGS) $(BIB_SRC)
	$(TEX) $(COMMON_FLAGS) $(TEX_FLAGS) $(TEX_SRC)
	$(TEX) $(COMMON_FLAGS) $(TEX_FLAGS) $(TEX_SRC)

clean:
	$(RM) -r $(BUILD_DIR)
