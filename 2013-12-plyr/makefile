all: notes exercises

notes:
	Rscript -e "knitr::knit('plyr-notes.Rmd')"
	perl -p -i -e "s/\`\`\`r/\`\`\`S/g" plyr-notes.md

exercises:
	Rscript -e "knitr::knit('plyr-exercises-answers.Rmd')"
	perl -p -i -e "s/\`\`\`r/\`\`\`S/g" plyr-exercises-answers.md
