# Extract posterior samples from a model fit.

A helper function to extract posterior samples across multiple chains
into a single data.frame.

## Usage

``` r
extract_samples(
  fit,
  inc_warmup = FALSE,
  inc_lp = FALSE,
  as.list = FALSE,
  unbounded = FALSE
)
```

## Arguments

- fit:

  A list returned by `sample_snuts`.

- inc_warmup:

  Whether to extract the warmup samples or not (default). Warmup samples
  should never be used for inference, but may be useful for diagnostics.

- inc_lp:

  Whether to include a column for the log posterior density (last
  column). For diagnostics it can be useful.

- as.list:

  Whether to return the samples as a list (one element per chain). This
  could then be converted to a CODA mcmc object.

- unbounded:

  Boolean flag whether to return samples in unbounded (untransformed)
  space. This can be useful for model debugging.

## Value

If as.list is FALSE, an invisible data.frame containing samples (rows)
of each parameter (columns). If multiple chains exist they will be
rbinded together, maintaining order within each chain. If as.list is
TRUE, samples are returned as a list of matrices.

## Details

This function is loosely based on the rstan function `extract`. Merging
samples across chains should only be used for inference after
appropriate diagnostic checks. Do not calculate diagnostics like Rhat or
effective sample size after using this function, instead, use
[`summarize_draws`](https://mc-stan.org/posterior/reference/draws_summary.html).
Likewise, warmup samples are not valid and should never be used for
inference, but may be useful in some cases for diagnosing issues.

## Examples

``` r
## A previously run fitted TMB model
fit <- readRDS(system.file('examples', 'fit.RDS', package='SparseNUTS'))
post <- extract_samples(fit)
tail(apply(post, 2, median))
#>          x1          x2          x3     xvec[1]     xvec[2] 
#>  0.03341737 -0.05535200  0.03685913 -0.01604522  0.02937307 
```
