BLOCK_RANGE_PAGES = \
	docs/block-range-1.html \
	docs/block-range-2.html \
	docs/block-range-3.html \
	docs/block-range-4.html \
	docs/block-range-5.html

default: docs/unicode.css $(BLOCK_RANGE_PAGES)

docs/unicode.css: docs/unicode.scss
	sassc "$<" >"$@.tmp"
	mv "$@.tmp" "$@"

docs/block-range-1.html: docs/block-range-1.ssi.html docs/block-range-1.inc.html
	ssi "$<" >"$@.tmp"
	mv "$@.tmp" "$@"

docs/block-range-2.html: docs/block-range-2.ssi.html docs/block-range-2.inc.html
	ssi "$<" >"$@.tmp"
	mv "$@.tmp" "$@"

docs/block-range-3.html: docs/block-range-3.ssi.html docs/block-range-3.inc.html
	ssi "$<" >"$@.tmp"
	mv "$@.tmp" "$@"

docs/block-range-4.html: docs/block-range-4.ssi.html docs/block-range-4.inc.html
	ssi "$<" >"$@.tmp"
	mv "$@.tmp" "$@"

docs/block-range-5.html: docs/block-range-5.ssi.html docs/block-range-5.inc.html
	ssi "$<" >"$@.tmp"
	mv "$@.tmp" "$@"

docs/block-range-1.inc.html: bin/block-table Makefile; bin/block-table range U+0000  U+1FFF   >"$@.tmp" && mv "$@.tmp" "$@"
docs/block-range-2.inc.html: bin/block-table Makefile; bin/block-table range U+2000  U+4DFF   >"$@.tmp" && mv "$@.tmp" "$@"
docs/block-range-3.inc.html: bin/block-table Makefile; bin/block-table range U+A000  U+FFFF   >"$@.tmp" && mv "$@.tmp" "$@"
docs/block-range-4.inc.html: bin/block-table Makefile; bin/block-table range U+10000 U+1CFFF  >"$@.tmp" && mv "$@.tmp" "$@"
docs/block-range-5.inc.html: bin/block-table Makefile; bin/block-table range U+1D000 U+10FFFF >"$@.tmp" && mv "$@.tmp" "$@"

clean:
	rm $(BLOCK_RANGE_PAGES) docs/unicode.css || true

.PHONY: default clean
