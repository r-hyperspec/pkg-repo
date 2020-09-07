# pkg-repo

[![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)

Welcome to `pkg-repo`.  This is a repository holding certain packages in the `r-hyperspec` series (in particular, data-rich packages that are too large to be distributed on CRAN, and also development packages). Developers: instructions about how to administer this repo are in `CONTRIBUTING.md`.

If you want to install a package, simply do the following:

```r
install.packages("hySpc.read.txt",
  repos = c("https://r-hyperspec.github.io/pkg-repo/", getOption("repos")))
```

Packages currently residing here:

- **hyperSpec** 0.100.0
