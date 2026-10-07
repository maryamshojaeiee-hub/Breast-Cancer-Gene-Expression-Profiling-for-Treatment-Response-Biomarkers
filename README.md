Can gene expression predict how breast cancer patients respond to chemotherapy? This project explores a public breast cancer microarray dataset (GEO: GSE25066) to find which clinical variables carry a gene expression signal, identify differentially expressed genes, and build classifiers.

Homework for the course "Statistical and Computational Methods for Integrated Analysis", Master of Statistics and Data Science (Bioinformatics), Hasselt University, 2025–2026.

[Read the full report →](https://github.com/maryamshojaeiee-hub/Breast-Cancer-Gene-Expression-Profiling-for-Treatment-Response-Biomarkers/report.html) · [View the code →](codes/01_differential_expression.Rmd)

About the Project

The dataset contains 22,283 genes measured in breast tumour samples, of which 301 had a known treatment response. The analysis covered unsupervised exploration with spectral maps, gene filtering, differential expression with limma (including a model adjusted for ER status and tumour grade), classification with nested loop cross-validation (DLDA, random forest, bagging, PAM and SVM), and pathway analysis with MLP.

Main finding: ER status was the dominant source of variation and could be predicted with high accuracy from only about 10 genes. Treatment response showed a much weaker signal, and part of it was explained by ER status and tumour grade; classifiers for response reached an error rate of about 30%.

## Reproducing the Analysis
The data are publicly available from GEO (GSE25066). Open report.qmd in RStudio and click Render. The main packages used are:

```r
install.packages(c("tidyverse", "knitr", "kableExtra"))
if (!requireNamespace("BiocManager", quietly = TRUE)) install.packages("BiocManager")
BiocManager::install(c("GEOquery", "Biobase", "limma", "a4", "nlcv", "MLP"))
```

## Tools
R, Quarto, limma, nlcv, MLP, Bioconductor

## Author
Maryam Shojaei Shahrokhabadi · [LinkedIn](https://www.linkedin.com/in/maryam-shojaei-210740250)· [maryam.shojaei.ee@gmail.com]
