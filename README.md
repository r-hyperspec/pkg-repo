# hySpc.pkgs

Welcome!

This is a repository holding certain packages in the [**`r-hyperspec`**](https://r-hyperspec.github.io/) series (in particular, data-rich packages that are too large to be distributed on CRAN, and also development packages).

**For developers:** The instructions about how to administer this repo are in [`CONTRIBUTING.md`](https://github.com/r-hyperspec/hySpc.pkgs/blob/gh-pages/CONTRIBUTING.md).

**For users:** If you want to install a package, simply use function `install.packages()` with the additional repository added as shown in this example:

```r
repos <- c("https://r-hyperspec.github.io/hySpc.pkgs/", getOption("repos"))
install.packages("name_of_package_of_interest", repos = repos)
```

Packages currently residing here:

Package       | Version       | Updated on    
------------- | ------------- | ------------- 
hySpc.ggplot2 | 0.0.0.9000 | 2020-08-20
hySpc.read.txt | 0.0.0.9001 | 2020-08-20

Previous (archived) versions of the packages residing here: 

Package       | Version       | Archived on   
------------- | ------------- | ------------- 
hyperSpec | 0.0.0.9000 | 2020-08-24
hySpc.ggplot2 | 0.0.0.5000 | 2020-08-20
hySpc.read.txt | 0.0.0.9000 | 2020-08-18
