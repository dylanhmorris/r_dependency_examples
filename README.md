# r_dependency_examples

Some non-functional R packages for testing purposes

## R package dependencies

* `package1` depends on local `package2` and `package3` (tar.gz)
     * refered to in Imports and in Remotes field (with relative paths assuming that the repo root is the working directory)
* `package1`, `package2` and `package3` all depend on one or more CRAN packages
* `package1` depends on a package from github (in particular one that is a subdirectory of the repository)
* `package4` is a version of `package1` that doesn't depend on `package2` or `package3`. `remotes::install_local()` succeeds with a named Github remote specified in the form `<name>=<repo>/<subdir>`
* `package5` is a version of `package4` for which `remotes::install_local()` fails because it uses `<name>=github::<repo>/<subdir>` syntax instead of the `<name>=<repo>/<subdir>` syntax.

## System requirements

* Each of the packages have one or more system requirements in their SystemRequirements field 
