# Package index

## All functions

- [`as.data.frame(`*`<snutsfit>`*`)`](https://noaa-afsc.github.io/SparseNUTS/reference/as.data.frame.snutsfit.md)
  :

  Convert object of class snutsfit to data.frame. Calls
  `extract_samples`

- [`as.tmbfit()`](https://noaa-afsc.github.io/SparseNUTS/reference/as.tmbfit.md)
  : Construtor for tmbfit objects

- [`benchmark_metrics()`](https://noaa-afsc.github.io/SparseNUTS/reference/benchmark_metrics.md)
  : Calculate gradient timings on a model for different metrics

- [`check_snuts_diagnostics()`](https://noaa-afsc.github.io/SparseNUTS/reference/check_snuts_diagnostics.md)
  : Check NUTS diagnostics of a fitted model

- [`.check_console_printing()`](https://noaa-afsc.github.io/SparseNUTS/reference/dot-check_console_printing.md)
  : Check if the session is interactive or Rstudio which has
  implications for parallel output

- [`.get_Q()`](https://noaa-afsc.github.io/SparseNUTS/reference/dot-get_Q.md)
  : Get the joint precision matrix Q from an optimized TMB or RTMB obj.

- [`.get_Qinv()`](https://noaa-afsc.github.io/SparseNUTS/reference/dot-get_Qinv.md)
  : Get the joint covariance Sigma from an optimized TMB or RTMB obj
  without random effects.

- [`.get_inits()`](https://noaa-afsc.github.io/SparseNUTS/reference/dot-get_inits.md)
  : Get a single initial value vector in untransformed model space

- [`.get_inputs()`](https://noaa-afsc.github.io/SparseNUTS/reference/dot-get_inputs.md)
  : Prepare inputs for sparse sampling

- [`.make_unique_names()`](https://noaa-afsc.github.io/SparseNUTS/reference/dot-make_unique_names.md)
  : Function to take a character vector of parameter names and force
  them to be unique by appending numbers in square brackets as needed

- [`.print.mat.stats()`](https://noaa-afsc.github.io/SparseNUTS/reference/dot-print.mat.stats.md)
  : Print matrix stats

- [`.rotate_posterior()`](https://noaa-afsc.github.io/SparseNUTS/reference/dot-rotate_posterior.md)
  : Update algorithm for mass matrix.

- [`.rotate_space()`](https://noaa-afsc.github.io/SparseNUTS/reference/dot-rotate_space.md)
  : Update algorithm for mass matrix.

- [`extract_sampler_params()`](https://noaa-afsc.github.io/SparseNUTS/reference/extract_sampler_params.md)
  : Extract sampler parameters from a fit.

- [`extract_samples()`](https://noaa-afsc.github.io/SparseNUTS/reference/extract_samples.md)
  : Extract posterior samples from a model fit.

- [`get_post()`](https://noaa-afsc.github.io/SparseNUTS/reference/get_post.md)
  : Extract posterior samples from a tmbfit object

- [`is.snutsfit()`](https://noaa-afsc.github.io/SparseNUTS/reference/is.snutsfit.md)
  : Check object of class snutsfit

- [`launch_shinytmb()`](https://noaa-afsc.github.io/SparseNUTS/reference/launch_shinytmb.md)
  : Launch shinystan for a TMB fit.

- [`pairs(`*`<snutsfit>`*`)`](https://noaa-afsc.github.io/SparseNUTS/reference/pairs.snutsfit.md)
  : Plot pairwise parameter posteriors and optionally the MLE points and
  confidence ellipses.

- [`plot(`*`<snutsfit>`*`)`](https://noaa-afsc.github.io/SparseNUTS/reference/plot.snutsfit.md)
  : Plot object of class snutsfit

- [`plot_Q()`](https://noaa-afsc.github.io/SparseNUTS/reference/plot_Q.md)
  : Make an image plot showing the correlation (lower triangle) and
  sparsity (upper triangle).

- [`plot_marginals()`](https://noaa-afsc.github.io/SparseNUTS/reference/plot_marginals.md)
  : Plot marginal distributions for a fitted model

- [`plot_sampler_params()`](https://noaa-afsc.github.io/SparseNUTS/reference/plot_sampler_params.md)
  : Plot adaptation metrics for a fitted model.

- [`plot_uncertainties()`](https://noaa-afsc.github.io/SparseNUTS/reference/plot_uncertainties.md)
  : Plot MLE vs MCMC marginal standard deviations for each parameter

- [`print(`*`<snutsfit>`*`)`](https://noaa-afsc.github.io/SparseNUTS/reference/print.snutsfit.md)
  : Print summary of snutsfit object

- [`sample_inits()`](https://noaa-afsc.github.io/SparseNUTS/reference/sample_inits.md)
  : Function to generate random initial values from a previous fit using
  SparseNUTS

- [`sample_snuts()`](https://noaa-afsc.github.io/SparseNUTS/reference/sample_snuts.md)
  : NUTS sampling for TMB models using a sparse metric (BETA).

- [`snutsfit()`](https://noaa-afsc.github.io/SparseNUTS/reference/snutsfit.md)
  : Constructor for the "snutsfit" (A-D fit) class

- [`summary(`*`<snutsfit>`*`)`](https://noaa-afsc.github.io/SparseNUTS/reference/summary.snutsfit.md)
  : Print summary of object of class snutsfit
