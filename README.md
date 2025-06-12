[![DOI](https://zenodo.org/badge/863505701.svg)](https://doi.org/10.5281/zenodo.15653268)

# Foram_OA

This git repository is designed to guide to user through the analysis of X-Ray microscopy data from foraminifera incubated under different ocean acidification conditions. This analysis has two steps:
1. setup of the git repository with appropriate data downloads
2. Run the analysis using the provided rmarkdown document

## Data download

The data for this analysis is hosted on [figshare](https://figshare.com/account/login#/projects/221938). Download the data with the desired method (_e.g._ direct download, curl, figshare api, etc), move them into the current working directory at the top of the git repository, and decompress the data using the following command 
```
tar -vzf waterAnalysis.tar.gz -c waterAnalysis
tar -xvzf thicknessData.tar.gz
mkdir thicknessAnalysis
mv OA*.csv thicknessAnalysis/
```

At this point, all of the data should be prepared for analysis.

## Running the analysis

There is an Rmarkdown file that is called Analysis_Markdown.rmd. It is recommended to open this file in Rstudio for analysis; however, running this analysis locally can consume large computational resources and may not be viable. Therefore, it is recommended to run this analysis on an HPC cluster and utilize Rstudio using a resource such as [open on demand](https://openondemand.org/) or by threading Rstudio from a cluster using singularity (A useful guide may be found [here](https://www.c4.ucsf.edu/howto/rstudio-server.html))
