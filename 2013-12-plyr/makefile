all: notes

notes:
	Rscript -e "knitr::knit('plyr-notes.Rmd')"
	perl -p -i -e "s/\`\`\`r/\`\`\`S/g" plyr-notes.md
