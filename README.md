# Download **`r-hyperspec`** Family Packages

Welcome!

This is a repository holding certain R packages in the [**`r-hyperspec`**](https://r-hyperspec.github.io/) series (in particular, data-rich packages that are too large to be distributed on CRAN).

**For developers:** The instructions about how to administer this repo are in [`CONTRIBUTING.md`](https://github.com/r-hyperspec/pkg-repo/blob/gh-pages/CONTRIBUTING.md).

**For users:** If you want to install a package, simply use R function `install.packages()` with the additional repository added as shown in this example:

```r
repos <- c("https://r-hyperspec.github.io/pkg-repo/", getOption("repos"))
install.packages("hyperSpec", repos = repos, type = "source")
```

Instead of `"hyperSpec"`, you may use any name of a package that resides in this repository or on [CRAN](https://cran.rstudio.com/web/packages/index.html).
You may also use a vector of several package names.


<!-- list of packages: start | DO NOT REMOVE THIS LINE -->

Packages currently residing here:

Package          | Version      | Updated on    
---------------- | ------------ | ------------- 
hySpc.chondro    | 0.0.0.9000   | 2023-04-23
hySpc.dplyr      | 0.3.0        | 2022-03-27
hySpc.ggplot2    | 0.0.0.9000   | 2023-04-23
hySpc.read.ENVI  | 0.0.0.9000   | 2023-04-23
hySpc.read.jdx   | 1.0.0.0      | 2023-04-23
hySpc.read.mat   | 0.0.0.9000   | 2023-04-23
hySpc.read.spc   | 0.0.0.9001   | 2023-04-23
hySpc.read.spe   | 0.0.0.9000   | 2023-04-23
hySpc.read.txt   | 0.0.0.9000   | 2023-04-23
hySpc.testthat   | 0.2.1.9000   | 2023-04-23
hyperSpec        | 0.200.0.9000 | 2023-04-23

Previous (archived) versions of the packages residing here: 

Package          | Version      | Updated on    
---------------- | ------------ | ------------- 
hySpc.read.jdx   | 1.0.0        | 2023-04-23
hySpc.read.jdx   | 0.0.0.9000   | 2021-08-13
hySpc.read.spc   | 0.0.0.9000   | 2022-07-15
hyperSpec        | 0.100.0.9001 | 2021-08-21
hyperSpec        | 0.100.0.9000 | 2021-08-03

<p align="right"> 2023-04-23 19:57:24 UTC </p>
