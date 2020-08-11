
# Notes for hyperSpec Team Members

* Users install from `gh-pages` which displays `index.html` while `master` displays `README.md` to the end user.
* Instructions for end users to install are given in `README.md`.
* Other repos (e.g. `hySpc.read.txt`) can and will automatically deploy tar balls (as `.tar.gz` archives) to this site.  When that happens, the most recent version goes into `src/contrib` and older versions go to `archive/pkg_name`.
* Automatic deployment is controlled by, for example `hySpc.read.txt/.github/workflows/build_check_deploy.yaml`. Deployment is from the `master` branch for data packages (which rarely change) and from the `develop` branch for selected other packages.
* Package `drat` handles deploying to `hySpc.pkgs`.  If you look at `src/contrib` you will see the tar balls, a human-readible file (`PACKAGES`) and two machine-readible files (`PACKAGES.gz` and `PACKAGES.rds`).  These are the pieces necessary for `R` to use this as a repository.  The paper in the _R Journal_ on `drat` is very useful, but it hides the simplicity in some ways. `drat` simply keeps these three ancillary files up-to-date.

# Instructions and Details for hyperSpec Team Members

* Please keep branches `master` and `gh-pages` identical.  The automatic deployment does this for you.
* If you edit `README.md` make sure that `# hySpc.pkgs` is the first line and that you don't add anything after `Packages currently residing here:`.  The automatic deploy scripts copy these lines and everything between them, then add a directory listing and then save an updated version of `README.md`.
* To manually deploy to this repo, follow these steps on either of those (local) branches:
  + `library("drat")`
	+ `insertPackage(file = "path to full name of tar.gz", repodir = "point to top level of the local repo", action = "archive")`
	+ Push the branch you are on to the `hySpc.pkgs` remote, to both the `master` and `gh-pages` branches.  It is essential that these two branches be the same or the automatic deployment fail with `git` "can't merge" issues.
* If you need to delete a package from this repo, be careful.  The best procedure seems to be to manually remove the `tar.gz` files, then insert another package (done via `R`).  Although it does not seem to be documented, inserting a package will update the ancillary files, removing info about the deleted packages.  If all packages are removed, it looks like the automatic deployment will fail (I don't see quite why, and am not certain this is the cause of some behaviors I have observed).  In this case, build a file of interest in the original repo, then manually insert it as described above.  Note that the unreleased version of `drat` on Github has a new function to remove packages (`updateRepo`), but I had trouble getting it to work (which could have been my fault, there were several problems present at the same time).
* Pulling from the remote can be problematic if automatic deployment has occurred.  Git knows the `.tar.gz` are different but of course it is not able to sync a binary file: `warning: Cannot merge binary files:` _Therefore .tar.gz files are git-ignored_.

Problems?  Let me know and I'll try to help!  Bryan
