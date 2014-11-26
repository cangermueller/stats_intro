
sub_rnw = $(wildcard */main.Rnw)

pdf: main.pdf

main.pdf: main.Rnw $(sub_rnw)
	Rscript -e "library(knitr); knit2pdf('$<')"


tmp_ext = aux bbl blg fdb_latexmk fls log nav out dnm toc vrb snm pdf

del = $(addprefix main., $(tmp_ext))
del += $(addprefix */main., $(tmp_ext))
clean:
	rm -f $(del)
