# Extract sampler parameters from a fit.

Extract information about NUTS trajectories, such as acceptance ratio
and treedepth, from a fitted object.

## Usage

``` r
extract_sampler_params(fit, inc_warmup = FALSE)
```

## Arguments

- fit:

  A list returned by `sample_snuts`.

- inc_warmup:

  Whether to extract the warmup samples or not (default). Warmup samples
  should never be used for inference, but may be useful for diagnostics.

## Value

An invisible data.frame containing samples (rows) of each parameter
(columns). If multiple chains exist they will be rbinded together.

## Details

Each trajectory (iteration) in NUTS has associated information about the
trajectory: stepsize, acceptance ratio, treedepth, and number of
leapfrog steps. This function extracts these into a data.frame, which
may be useful for diagnosing issues in certain cases. In general, the
user should not need to examine them, or preferably should via
[`plot_sampler_params`](https://noaa-afsc.github.io/SparseNUTS/reference/plot_sampler_params.md)
or
[`launch_shinytmb`](https://noaa-afsc.github.io/SparseNUTS/reference/launch_shinytmb.md).

## See also

[`launch_shinytmb`](https://noaa-afsc.github.io/SparseNUTS/reference/launch_shinytmb.md).

## Examples

``` r
fit <- readRDS(system.file('examples', 'fit.RDS', package='SparseNUTS'))
sp <- extract_sampler_params(fit, inc_warmup=TRUE)
str(sp)
#> 'data.frame':    1000 obs. of  8 variables:
#>  $ chain        : num  1 1 1 1 1 1 1 1 1 1 ...
#>  $ iteration    : num  1 2 3 4 5 6 7 8 9 10 ...
#>  $ accept_stat__: num  0.00 4.35e-38 1.00 9.97e-01 1.00 ...
#>  $ stepsize__   : num  4 2.335 0.23 0.24 0.322 ...
#>  $ treedepth__  : num  0 1 4 4 4 3 2 3 2 2 ...
#>  $ n_leapfrog__ : num  1 1 15 15 15 7 3 7 3 3 ...
#>  $ divergent__  : num  1 0 0 0 0 0 0 0 0 0 ...
#>  $ energy__     : num  19.5 18 17.7 14.8 14.4 ...
```
