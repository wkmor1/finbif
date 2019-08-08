
# finbif <img src="man/figures/logo.png" align="right" alt="" width="120">

[![Project Status: WIP – Initial development is in progress, but there
has not yet been a stable, usable release suitable for the
public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)
[![Build
Status](https://travis-ci.com/luomus/finbif.svg?branch=master)](https://travis-ci.com/luomus/finbif)
[![AppVeyor build
status](https://ci.appveyor.com/api/projects/status/github/luomus/finbif?branch=master&svg=true)](https://ci.appveyor.com/project/luomus/finbif/branch/master)
[![codecov](https://codecov.io/gh/luomus/finbif/branch/master/graph/badge.svg)](https://codecov.io/github/luomus/finbif/branch/master)

An R interface to the FinBIF (Finnish Biodiversity Information Facility)
API (api.laji.fi).

## Installation

You can install the development version of finbif from
[GitHub](https://github.com),

``` r
remotes::install_github("luomus/finbif")
```

## Documentation

Read the online documentation [here](https://luomus.github.io/finbif).

## Getting a FinBIF access token

First load the finbif R package.

``` r
library(finbif)
```

To use the FinBIF API you must first request and set a personal access
token. You can request an API token to be sent to your email address
with the function `finbif_get_token`.

``` r
finbif_request_token("your@email.com")
```

Copy the access token that was sent to your email and set it as the
environment variable `FINBIF_ACCESS_TOKEN` either for the current
session,

``` r
Sys.setenv(
  FINBIF_ACCESS_TOKEN = "xtmSOIxjPwq0pOMB1WvcZgFLU9QBklauOlonWl8K5oaLIx8RniJLrvcJU4v9H7Et"
)
# Note: the above is not a real access token. Do not try using it.
```

, or by adding it to a `Renviron` startup file (see
[here](https://rviews.rstudio.com/2017/04/19/r-for-enterprise-understanding-r-s-startup/)
for details).

## Usage

Download occurrence data from finbif.

``` r
finbif_occurrence("Cygnus cygnus", n = 100)
```

-----

## Contributing

Development is a community effort, and we encourage participation.
Please read [the contribution guide](CONTRIBUTING.md) for details.

Please note that the ‘finbif’ project is released with a [Contributor
Code of Conduct](CODE_OF_CONDUCT.md). By contributing to this project,
you agree to abide by its terms.
