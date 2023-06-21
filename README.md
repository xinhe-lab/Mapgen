
<!-- README.md is generated from README.Rmd. Please edit that file -->

## Mapgen

<!-- badges: start -->
<!-- badges: end -->

`mapgen` is an R package that performs gene mapping based on
functionally-informed genetic fine-mapping.

## Installation

You can install the development version of `mapgen` from
[GitHub](https://github.com/xinhe-lab/mapgen) with:

``` r
# install.packages("remotes")
remotes::install_github("kevinlkx/mapgen")
```

- Please install `susieR` package, if you want to run finemapping with
  GWAS summary statistics using SuSiE.
- Please install [TORUS](https://github.com/xqwen/torus) software
  package, if you want to run enrichment analysis using TORUS.

After installing, check that it loads properly:

``` r
library(mapgen)
```

## Overview of the workflow

**Example workflow from our heart single-cell study:**

We developed an integrated procedure that combines single-cell genomics
with novel computational approaches to study genetics of complex traits.

Main steps:

1.  Obtain cell-type-resolved open chromatin regions (OCRs) using
    scATAC-seq and snRNA-seq.
2.  Assess the enrichment of genetic signals of a trait of interest in
    OCRs across all the cell types.
3.  Perform Bayesian statistical fine mapping on trait-associated loci,
    using a informative prior that favors likely functional variants
    located in OCRs of enriched cell types.
4.  Assign the likely cell type(s) through which the causal variants act
    in most loci using fine-mapped SNPs and its associated cell type
    information.
5.  Use our novel gene mapping procedure to infer causal genes at each
    locus.

<div class="figure">

<img src="man/figures/workflow.overview.png" alt="Overview of the workflow" width="75%" />
<p class="caption">
Overview of the workflow
</p>

</div>

Please follow the
[tutorials](https://kevinlkx.github.io/mapgen/articles/index.html) to
learn how to use the package.

## Reference

Alan Selewa\*, Kaixuan Luo\*, Michael Wasney, Linsin Smith, Xiaotong
Sun, Chenwei Tang, Heather Eckart, Ivan Moskowitz, Anindita Basu, Xin
He, Sebastian Pott. Single-cell genomics improves the discovery of risk
variants and genes of Atrial Fibrillation. medRxiv 2022.02.02.22270312;
doi: <https://doi.org/10.1101/2022.02.02.22270312>
