
<!-- README.md is generated from README.Rmd. Please edit that file -->

# BayesfMRI

<!-- badges: start -->

[![R-CMD-check](https://github.com/mandymejia/BayesfMRI/workflows/R-CMD-check/badge.svg)](https://github.com/mandymejia/BayesfMRI/actions)
[![Codecov test
coverage](https://codecov.io/gh/mandymejia/BayesfMRI/branch/master/graph/badge.svg)](https://app.codecov.io/gh/mandymejia/BayesfMRI?branch=master)
<!-- badges: end -->

`BayesfMRI` R package. Includes the main function `BayesGLM`, which
implements the spatial Bayesian GLM for task fMRI on the cortical
surface proposed by Mejia et al. 2019a
\[<https://doi.org/10.1080/01621459.2019.1611582>\]. Also contains two
wrapper functions:

-   `BayesGLM_cifti` – implements `BayesGLM` on CIFTI-format
    (greyordinates) fMRI data
-   `BayesGLM_slice` - implements `BayesGLM` on slice-wise volumetric
    fMRI data

## Citation

If you use `BayesfMRI`, please cite our
[paper](https://doi.org/10.1080/01621459.2019.1611582). You can also
obtain citation information from within R like so:

``` r
citation("BayesfMRI")
```

    ## 
    ## To cite BayesfMRI in publications, please use:
    ## 
    ## For the spatial Bayesian GLM for task fMRI on the cortical surface,
    ## please cite:
    ## 
    ##   Mejia, A. F., Yue, Y., Bolin, D., Lindgren, F., & Lindquist, M. A.
    ##   (2020). A Bayesian general linear modeling approach to cortical
    ##   surface fMRI data analysis. Journal of the American Statistical
    ##   Association, 115(530), 501-520.
    ## 
    ## A BibTeX entry for LaTeX users is
    ## 
    ##   @Article{,
    ##     title = {A {B}ayesian general linear modeling approach to cortical surface {fMRI} data analysis},
    ##     author = {Amanda F. Mejia and Yu (Ryan) Yue and David Bolin and Finn Lindgren and Martin A. Lindquist},
    ##     year = {2020},
    ##     journal = {Journal of the American Statistical Association},
    ##     pages = {501-520},
    ##     volume = {115},
    ##     number = {530},
    ##     publisher = {Taylor and Francis},
    ##     doi = {https://doi.org/10.1080/01621459.2019.1611582},
    ##   }

## Important Note on Dependencies:

`BayesfMRI` depends on the `ciftiTools` package, which requires an
installation of Connectome Workbench. It can be installed from the [HCP
website](https://www.humanconnectome.org/software/get-connectome-workbench).

<!-- The INLA package is required, which, due to a CRAN policy, will not be installed automatically. You can obtain it by running `install.packages("INLA", repos=c(getOption("repos"), INLA="https://inla.r-inla-download.org/R/stable"), dep=FALSE)`.  The default R-INLA binaries are built on Ubuntu1604. Instructions on how to obtain binaries for other Linux builds are available at https://www.r-inla.org/events/alternativelinuxbuilds.  **Note: INLA must be installed before installing `BayesfMRI`.**

An INLA-PARDISO license is also required for computational efficiency.  To obtain an INLA-PARDISO license, run `inla.pardiso()` in R after running `library(INLA)`. Once you obtain a license, point to it using `INLA::inla.setOption(pardiso.license = "pardiso.lic")` followed by `INLA::inla.pardiso.check()` to ensure that PARDISO is successfully installed and running. -->
