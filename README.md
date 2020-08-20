# hySpc.pkgs

[![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)

Welcome to `hySpc.pkgs`.  This is a repository holding certain packages in the `r-hyperspec` series (in particular, data-rich packages that are too large to be distributed on CRAN, and also development packages). Developers: instructions about how to administer this repo are in `CONTRIBUTING.md`.

If you want to install a package, simply do the following:

```r
repos <- c("https://r-hyperspec.github.io/hySpc.pkgs/", getOption("repos"))
install.packages("hyperSpec", repos = repos)
```

Packages currently residing here:

- **hyperSpec** 0.100.0 _(2020-08-19)_


Previous (archived) versions of the packages residing here:
