# Plot MLE vs MCMC marginal standard deviations for each parameter

Plot MLE vs MCMC marginal standard deviations for each parameter

## Usage

``` r
plot_uncertainties(fit, log = TRUE, plot = TRUE)
```

## Arguments

- fit:

  A fitted object returned by
  [`sample_snuts`](https://noaa-afsc.github.io/SparseNUTS/reference/sample_snuts.md)

- log:

  Whether to plot the axes in log space (default TRUE).

- plot:

  Whether to plot it or not.

## Value

Invisibly returns data.frame with parameter name (row) and estimated
uncertainties for each method (columns).

## Details

It can be helpful to compare uncertainty estimates between the two
paradigms. This plots the marginal posterior standard deviation vs the
frequentist standard error estimated from the .cor file. Large
differences often indicate issues with one estimation method.

## Examples

``` r
fit <- readRDS(system.file('examples', 'fit.RDS', package='SparseNUTS'))
x <- plot_uncertainties(fit, plot=FALSE)
head(x)
#>             par   sd.post sd.mle
#> x1           x1 0.9988344      1
#> x2           x2 2.0190329      2
#> x3           x3 2.9297466      3
#> xvec[1] xvec[1] 1.0397279      1
#> xvec[2] xvec[2] 1.0453499      1
```
