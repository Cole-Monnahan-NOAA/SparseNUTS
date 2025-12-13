# Check NUTS diagnostics of a fitted model

Check NUTS diagnostics of a fitted model

## Usage

``` r
check_snuts_diagnostics(fit, print = TRUE)
```

## Arguments

- fit:

  A fitted SNUTS object

- print:

  Whether to print the results to console

## Value

A data.frame containing diagnostic results (invisibly)

## Details

This is a wrapper which calls the function
`StanEstimators::check_hmc_diagnostics`
