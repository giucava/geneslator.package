
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Geneslator

<!-- badges: start -->
<!-- badges: end -->

This package allows the user to convert gene Ensembl IDs into gene
symbols or Entrez IDs for Homo sapiens and Mus musculus.

## Installation

You can install the development version of Geneslator from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("knowmics-lab/geneslator")
```

## Example

``` r
library(Geneslator)
```

``` r
#Homo sapiens

list_ensembl <- c("ENSG00000139618", "ENSG00000157764")
keyid <- "ENSEMBL"
outputid <- c("ENSEMBL", "SYMBOL")
conversion_result <- conversion_id_genes(list_ensembl, keyid, outputid)

#Mus musculus
list <- c("Pzp","Igkv13-84")
keyid <- "SYMBOL"
outputid <- c("ENSEMBL", "SYMBOL", "Gene.type", "ENTREZID","Alias")
conversion_result_mouse <- conversion_id_genes_mouse(list_ensembl, keyid, outputid)
```
