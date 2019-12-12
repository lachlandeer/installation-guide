# R


## Install R

We can install `R` as follows:

```{bash}
apt-get install r-base r-base-dev
```

## Verify R Install

```{R}
R --version
```

which yields:

```{out}
R version 3.6.1 (2019-07-05) -- "Action of the Toes"
Copyright (C) 2019 The R Foundation for Statistical Computing
Platform: x86_64-pc-linux-gnu (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under the terms of the
GNU General Public License versions 2 or 3.
For more information about these matters see
https://www.gnu.org/licenses/.
```

## OpenBlas support 

One may want to have the automatically the multi-threaded OpenBlas library installed in order to get higher performance for linear algebra operations:

```{bash}
apt-get install libopenblas-base
```

## RStudio

RStudio is a GUI for `R`.

Install by downloading from the [website](https://rstudio.com/products/rstudio/download/#download) and then installing via the Ubuntu software installer.

## R Packages

Here's my basic set of packages that I install so that I can do most of what I want straight off the bat:

Via the `install.packages` command in R:

```{r}
to_install <-c( "reshape", "rmarkdown",
                "plm", "Hmisc", "sandwich",
                "Ecdat", "stargazer", "knitr",
                "httr", "rvest", "xml2",
                "xtable","tidyverse", "AER",
                "rdd", "car", "aod", "lmtest",
                "lfe", "nlme", "lme4",
                "erer", "margins", "multiwayvcov"
                "lubridate", "haven", "rddensity",
                "rdrobust", "ivpack", "readxl",
                "ggrepel", "multiwayvcov", "RSQLite", 
                "dbplyr", "devtools", "blogdown", 
                "rticles", "packrat", "here",
                "optparse", "rlist"
                )

install.packages(to_install)
```

Note that many dependencies get installed along the way.

I also want some packages to be installed from Github - these typicall arent on CRAN yet:

```{r}
from_gh <- c("ddsjoberg/gtsummary", 
             "vincentarelbundock/modelsummary", 
             "rstudio/fontawesome", 
             "rstudio/gt",
             "rstudio/renv"
             )

devtools::install_github(from_gh)
```
