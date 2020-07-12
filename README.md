# hySpc.pkgs

[![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)

Welcome to `hySpc.pkgs`.  This is a repository holding certain packages in the `r-hyperspec` series (in particular, data-rich packages that are too large to be distributed on CRAN).

If you want to install a package, simply do the following:

```r
install.packages("drat") # only if not already installed
library("drat")
addRepo("github.com/r-hyperspec/hySpc.pkgs")
install.packages("hySpc.read.Witec")
```

Packages currently residing here:

* hySpc.read.Witec_0.0.0.0001.tar.gz (testing example)
* More coming soon!
