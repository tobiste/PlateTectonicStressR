<!-- badges: start -->
[![CRAN status](https://www.r-pkg.org/badges/version/tectonicr)](https://CRAN.R-project.org/package=tectonicr)
[![R-CMD-check](https://github.com/tobiste/tectonicr/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/tobiste/tectonicr/actions/workflows/R-CMD-check.yaml)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.8372508.svg)](https://doi.org/10.5281/zenodo.8372508)
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)
<!-- badges: end -->

# tectonicr

**tectonicr** is a free and open-source **R** package for modeling and analyzing the direction of the maximum horizontal stress (SHmax) based on the empirical link between the direction of intraplate stress and the direction of the relative motion of neighboring plates (Wdowinski, 1998; Stephan et al., 2023). The following methods are available:

- **Direction of the plate boundary forces**: `PoR_shmax()` gives the predicted stress field adjacent to a plate boundary, calculated using the relative plate motion of the neighboring plates using the function `model_shmax()`. The goodness-of-fit can be statistically tested by e.g. `norm_chisq()`, `circular_dispersion()` ,`rayleigh_test()`, and `confidence_interval()`.
- **Distance to plate boundary**: `distance_from_pb()` gives the distance between the stress data point and the plate boundary measured along the stress trajectories.
- **Trajectories of the theoretical stress field**  `eulerpole_paths()` generates an  `sf` object containing spatial information that is suitable to plot with, for instance, `ggplot()`. 
- **Relative rotations from a given set of plate motion parameters**: `equivalent_rotation()` transfers a set of plate motion parameters into the relative plate motions among the given plates. 
- **Average direction and variance of a set of SHmax data** using (weighted) statistics and other parameters to statistically estimate the distribution parameters of pi-directional data. 
- **Spatial interpolation of of SHmax**: `PoR_stress2grid()` uses distance, method, and quality-weighted mean direction of stress data without being affected by angular distortions.
- **Rose plot** `rose()` shows the frequencies of the orientations in polar coordinates
- **Stress anomaly map**: spatial distribution of the dispersion of the observed stress field from the directions of plate boundary forces

## Prerequisites

You must have R installed on your system (see http://r-project.org). To install 
**tectonicr** from CRAN, type the following code at the R command line prompt:

```
install.packages("tectonicr")
```

## Installation

The most recent development version of **tectonicr** is available from Github 
and can be installed on your system as follows:

```
# install.packages("remotes") # install if needed
remotes::install_github('tobiste/tectonicr')
library('tectonicr')
```

## Documentation
https://tobiste.github.io/tectonicr/articles/tectonicr.html

## Author
Tobias Stephan

## How to cite
When referencing this package, please cite 

Stephan, T., Enkelmann, E., and Kroner, U. (2023). Analyzing the horizontal orientation of the crustal stress adjacent to plate boundaries. *Scientific Reports*, *13*(1). DOI: [10.1038/s41598-023-42433-2](https://doi.org/10.1038/s41598-023-42433-2).

and the package DOI: [10.5281/zenodo.8372508](https://doi.org/10.5281/zenodo.8372508).


## License
GPL-3.0 License
