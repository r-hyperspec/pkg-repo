
# Notes for hyperSpec Team Members

* Users install from `gh-pages` which displays `index.html` while `master` displays `README.md` to the end user.
* Instructions for end users to install are given in `README.md`.
* Other repos (currently: `hySpc.read.Witec`) can and will automatically deploy tar balls (as `.tar.gz` archives) to this site.  When that happens, the most recent version goes into `src/contrib` and older versions go to `archive/pkg_name`.
* Automatic deployment is controlled by, for example `hySpc.read.Witec/.github/workflows/build_check_deploy.yaml`. Deployment is from the `master` branch.
* Package `drat` handles deploying to `hySpc.pkgs`.  If you look at `src/contrib` you will see the tar balls, a human-readible file (`PACKAGES`) and two machine-readible files (`PACKAGES.gz` and `PACKAGES.rds`).  These are the pieces necessary for `R` to use this as a repository.  The paper in the _R Journal_ on `drat` is very useful, but it hides the simplicity in some ways. `drat` simply keeps these three ancillary files up-to-date.

# Instructions for hyperSpec Team Members

* Please keep branches `master` and `gh-pages` identical.
* To manually deploy to this repo, follow these steps on either of those (local) branches:
  + `library("drat")`
	+ `insertPackage(file = "path to full name of tar.gz", repodir = "point to top level of the local repo", action = "archive")`
	+ Push the branch you are on to the `hySpc.pkgs` remote, to both the `master` and `gh-pages` branches.
