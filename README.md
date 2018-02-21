# singularity-r
Singularity recipes for base-images containing R.

 * R is installed from source which is downloaded from [CRAN](https://cran.r-project.org/) (Comprehensive R Archive Network).
 * Packages needed to build R and those needed to run R like gfortran, g++ and gcc are installed through the debian repositories via `apt-get install`.
 * At the end of the build process the images is cleaned up by:
    * removing packages only needed for the build,
    * removing the package cache,
    * removing downloaded files used for the build.