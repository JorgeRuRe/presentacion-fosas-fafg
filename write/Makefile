#
# Authors:     OE & JRR
# Maintainers: OE & JRR
# Copyright:   2021, Ibero, Data Cívica, and HRDAG, GPL v2 or later
# ================================================================
#
# presentacion-fosas-fafg/write/Makefile
#

.PHONY: all

all: output/paper-fosas.pdf

clean:
	rm -r output/*

R_OPTS=--no-save --no-restore --no-init-file --no-site-file
KNIT="rmarkdown::render(input='$<', output_dir='output/')"

output/paper-fosas.pdf: \
		src/presentacion-fosas-fafg.Rmd
	Rscript $(R_OPTS) -e $(KNIT)
	-rm src/paper-fosas.log

# done.
