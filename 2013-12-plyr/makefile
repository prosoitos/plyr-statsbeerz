all: notes

notes:
	#Rscript -e "knitr::knit('plyr-notes.Rmd')"
	#perl -p -i -e "s/\`\`\`r/\`\`\`S/g" plyr-notes.md
	cp plyr-notes.Rmd temp.Rmd
	perl -p -i -e "s/\#\#/\#/g" temp.Rmd
	perl -p -i -e "s/\#\#\#/\#\#/g" temp.Rmd
	perl -p -i -e "s/\`\`\`{r/\`\`\`\n     \`\`\`{r/g" temp.Rmd
	pandoc -s temp.Rmd -o temp.Rnw -f markdown -t latex
	perl -p -i -e "s/     \`\`\`{r[ ]*([^}]*)}/<<\\1>>=/g" temp.Rnw
	perl -p -i -e "s/\\\begin{verbatim}\n//g" temp.Rnw
	perl -p -i -e "s/\\\end{verbatim}/@/g" temp.Rnw
	#Rscript -e "knitr::knit('temp.Rnw')"
	#pdflatex temp.tex
