#rule for making report
FinalProjectCode.html: data.csv FinalProjectCode.Rmd
	Rscript -e "rmarkdown::render('FinalProjectCode.Rmd')" 

#rule for cleaning data
data.csv: cleandata.R surveydata.xlsx
	chmod +x cleandata.R && \
	Rscript cleandata.R

#rule for installing packages
install:
	chmod +x InstallPackages.R && \
	Rscript InstallPackages.R

#rule for help
.PHONY: help
help: 
	@echo "FinalProjectCode.html: Generate final analysis report."
	@echo "install: Installed R packages needed for analysis."
	@echo "data.csv: Cleans raw dataset."