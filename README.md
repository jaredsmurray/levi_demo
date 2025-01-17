# ICHPS 2025 BART Workshop Materials

This repository hosts slides, data, and vignettes from the 2025 ICHPS BART Workshop.

## Software dependencies

### `stochtree` package

The `stochtree` R package is hosted on [Github](https://github.com/StochasticTree/stochtree) 
and has a dedicated docsite ([general](https://stochtree.ai) and [R-specific](https://stochtree.ai/R_docs/pkgdown/index.html)).

The package is not [*yet!*] on CRAN, but can be installed directly from Github with 
the `remotes` package as follows

```{r}
# install.packages("remotes")
remotes::install_github("StochasticTree/stochtree", ref="r-dev")
```

If you encounter issues with the above installation, it is potentially due to a missing / inaccessible C++ compiler. 
To troubleshoot, follow the instructions below for your platform.

#### MacOS

The recommended compiler toolchain for R packages on MacOS is `xcode`. 
[This page from CRAN](https://mac.r-project.org/tools/) explains how to install 
xcode, as well as any other common MacOS C++ dependencies.

#### Windows

CRAN ships a special compiler / developer software toolchain for Windows called "Rtools".
[This landing page](https://cran.r-project.org/bin/windows/) will help you find the proper version 
of Rtools for your system (it should be matched to your installed version of R, so if your R console 
says "R 4.4.2", then you should install [Rtools44](https://cran.r-project.org/bin/windows/Rtools/rtools44/rtools.html), 
and so on.)

### Possum package

The possum (POSterior SUMmarization) package is also available on Github and 
can be installed via `remotes::install_github`

```{r}
remotes::install_github("spencerwoody/possum")
```

### Other dependencies

The vignettes require several other packages which can be installed from CRAN

```{r}
pkg_list <- c("ggplot2", "latex2exp", "coda", "rpart", "rpart.plot", "tidyverse", "here")
install.packages(pkg_list)
```
