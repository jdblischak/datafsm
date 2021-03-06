## Test environments

* local build Windows 10, R 3.6.1
* ubuntu 18.04, R 3.6.1
* R-hub builder:
    * ubuntu 16.04, R-release GCC
    * ubuntu 16.04, R-devel GCC
    * macOS 10.11 El Capitan, R-release
    * debian, R-release GCC
    * debian, R-devel GCC
    * debian, R-patched GCC
* winbuilder devel, release, oldrelease.

## R CMD check results

* r-hub Debian R-devel build:

    0 errors | 0 warnings | 1 note

* All other builds:

    0 errors | 0 warnings | 0 notes

## NOTES

* **debian rhub R-devel** build gave a NOTE with false-positives for possible 
  spelling errors on the words "interpretable" and "stochasticity". Both words 
  are spelled correctly. 

* No NOTEs from other builds.

## Downstream dependencies

None.

## Additional comments

* The vignette FRD_vignette.Rmd takes a very long time to build.
* This submission is an update to version 0.2.3

    I have removed the dependency on the tidyverse package at the request of 
    the maintainer of that package and replaced it with dependencies on 
    component packages of tidyverse: dplyr, tidyr, and purrr.
