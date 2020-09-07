
# Notes for hyperSpec Team Members

* There is only one branch here: `gh-pages`.
* Instructions for end users to install are given in `README.md`.
* Other repos (e.g. `hySpc.read.txt`) can and will automatically deploy tar balls (as `.tar.gz` archives) to this site.  When that happens, the most recent version goes into `src/contrib` and older versions go to `archive/pkg_name`.
* Automatic deployment is controlled by, for example `hySpc.read.txt/.github/workflows/build_check_deploy.yaml`.
* Package `drat` handles deploying to `pkg-repo`.  If you look at `src/contrib` you will see the tar balls, a human-readible file (`PACKAGES`) and two machine-readible files (`PACKAGES.gz` and `PACKAGES.rds`).  These are the pieces necessary for `R` to use this as a repository.  The paper in the _R Journal_ on `drat` is very useful, but it hides the simplicity in some ways. `drat` simply keeps these three ancillary files up-to-date.

# Instructions and Details for hyperSpec Team Members

* If you edit `README.md` make sure that `# pkg-repo` is the first line and that you don't add anything after `Packages currently residing here:`.  There is a `yaml` in this repo that copies these lines and everything between them, adds a directory listing and then saves an updated version of `README.md`.
* To manually deploy to this repo, follow these steps:
  + `library("drat")`
	+ `insertPackage(file = "path to full name of tar.gz", repodir = "point to top level of the local repo", action = "archive")`
	+ Push the branch you are on to the `pkg-repo` remote.
* If you need to delete a package do so by the usual means.  The `yaml` herein will automatically update the indices.

Problems?  Let me know and I'll try to help!  Bryan
