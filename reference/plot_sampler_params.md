# Plot adaptation metrics for a fitted model.

Plot adaptation metrics for a fitted model.

## Usage

``` r
plot_sampler_params(fit, plot = TRUE)
```

## Arguments

- fit:

  A fitted object returned by
  [`sample_snuts`](https://noaa-afsc.github.io/SparseNUTS/reference/sample_snuts.md).

- plot:

  Whether to plot the results

## Value

Prints and invisibly returns a ggplot object

## Details

This utility function quickly plots the adaptation output of NUTS
chains.

## Examples

``` r
fit <- readRDS(system.file('examples', 'fit.RDS', package='SparseNUTS'))
plot_sampler_params(fit)
```
