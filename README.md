# Download **`r-hyperspec`** Family Packages

[![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)

Welcome!
This is a repository holding certain R packages in the [**`r-hyperspec`**](https://r-hyperspec.github.io/) series (in particular, data-rich packages that are too large to be distributed on CRAN, and also development packages).

**For developers:** The instructions about how to administer this repo are in [`CONTRIBUTING.md`](https://github.com/r-hyperspec/hySpc.pkgs/blob/gh-pages/CONTRIBUTING.md).

**For users:** If you want to install a package, simply use R function `install.packages()` with the additional repository added as shown in this example:

```r
repos <- c("https://r-hyperspec.github.io/hySpc.pkgs/", getOption("repos"))
install.packages("hyperSpec", repos = repos)
```

Packages currently residing here:

- **hyperSpec** 0.100.0 <font size=1>(2020-08-20)</font>
- **hySpc.ggplot2** 0.0.0.9000 <font size=1>(2020-08-20)</font>
- **hySpc.read.txt** 0.0.0.9001 <font size=1>(2020-08-20)</font>

Previous (archived) versions of the packages residing here: 

- **hySpc.ggplot2** 0.0.0.5000 <font size=1>(2020-08-20)</font>
- **hySpc.ggplot2** 0.0.0.1000 <font size=1>(2020-08-20)</font>
- **hySpc.read.txt** 0.0.0.9000 <font size=1>(2020-08-18)</font>
- **hySpc.read.txt** 0.0.0.2000 <font size=1>(2020-08-16)</font>
- **hySpc.read.txt** 0.0.0.1000 <font size=1>(2020-08-10)</font>
