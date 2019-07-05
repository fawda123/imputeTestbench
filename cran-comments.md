## Resubmission 

This is a resubmission for updates to a new release of a package dependency, imputeTS v3.0

## Test environments

* Ubuntu xenial 16.04.6 (on travis-ci), R 3.6.0
* local Windows 7 install, R 3.6.0
* local Windows 7 install, Current r-devel (2019-07-05 r76780)
* Windows install (on AppVeyor), R 3.6.0 Patched (2019-06-23 r76734)
* win-builder [http://win-builder.r-project.org/](http://win-builder.r-project.org/) (devel and release)

## R CMD check results

There was one ERROR on win-builder (for devel and release): Error: object 'na_interpolation' is not exported by 'namespace:imputeTS'.

The error is likely from an older version of imputeTS that is installed on win-builder.  The checks pass with v3.0 of imputeTS for all other test environmented listed above.

## Downstream dependencies

* WindCurves: No ERRORs, WARNINGs, or NOTEs found.
