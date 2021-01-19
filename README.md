
## imputeTestbench

#### *Neeraj Bokde, <neerajdhanraj@gmail.com>, Marcus W. Beck, <mbafs2012@gmail.com>*

[![R-CMD-check](https://github.com/fawda123/imputeTestbench/workflows/R-CMD-check/badge.svg)](https://github.com/fawda123/imputeTestbench/actions)
[![Downloads from the RStudio CRAN
mirror](http://cranlogs.r-pkg.org/badges/grand-total/imputeTestbench)](https://CRAN.R-project.org/package=imputeTestbench)

This is the development repository for the imputeTestbench package. This
package provides a testbench for comparing imputation methods for
missing data in univariate time series.

The development version of this package can be installed from GitHub:

``` r
install.packages('devtools')
library(devtools)
install_github('neerajdhanraj/imputeTestbench', ref = 'development')
```

The current release can be installed from CRAN:

``` r
install.packages('imputeTestbench')
```

Load the package after installation:

``` r
library(imputeTestbench)
```

#### Basic use

The core function is `impute_errors()`. See the help documentation for
more details.

``` r
a <- impute_errors(data = nottem)
a
```

    ## $Parameter
    ## [1] "rmse"
    ## 
    ## $MissingPercent
    ## [1] 10 20 30 40 50 60 70 80 90
    ## 
    ## $na.approx
    ## [1]  0.9745496  1.3856628  1.9129615  2.6498481  3.7849822  5.0208590  6.6343677
    ## [8]  8.4455223 10.3949327
    ## 
    ## $na.interp
    ## [1]  0.8221107  1.1478071  1.4159549  1.6452581  1.9016976  2.0818991  2.3455729
    ## [8]  2.6274192 10.3949327
    ## 
    ## $na_interpolation
    ## [1]  0.9745496  1.3856628  1.9129615  2.6498481  3.7849822  5.0208590  6.6343677
    ## [8]  8.4455223 10.3949327
    ## 
    ## $na.locf
    ## [1]  1.932793  3.029201  3.898818  5.166109  6.233874  7.593585  9.028926
    ## [8] 10.787879 11.841940
    ## 
    ## $na_mean
    ## [1] 2.634303 3.763457 4.630139 5.450282 6.089774 6.660770 7.192983 7.660656
    ## [9] 8.323775

``` r
plot_errors(a, plotType = 'line')
```

![](README_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

#### Citation

Beck MW, Bokde N, Ascencio-Cortes G, Kulat K (2018). “R package
imputeTestbench to Compare Imputation Methods for Univarite Time
Series.” *The R Journal*, *10*(1), 218-233. doi: 10.32614/RJ-2018-024
(URL: <http://doi.org/10.32614/RJ-2018-024>).

#### Bug reports

Please submit any bug reports (or suggestions) using the
[issues](https://github.com/neerajdhanraj/imputeTestbench/issues) tab of
the GitHub page.

#### License

This package is released in the public domain under the creative commons
license CC0.
