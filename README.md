<!-- README.md is generated from README.Rmd. Please edit that file -->

[![Build Status](https://travis-ci.org/JohnNay/fsm.png?branch=master)](https://travis-ci.org/JohnNay/fsm)

This R package -- by John Nay and Jonathan Gilligan -- implements our method for automatically generating models of dynamic decision-making that both have strong predictive power and are interpretable in human terms. This is useful for designing empirically grounded agent-based simulations and for gaining direct insight into observed dynamic processes. We use an efficient model representation and a genetic algorithm-based estimation process to generate simple deterministic approximations that explain most of the structure of complex stochastic processes. This method, implemented in C++ and R, scales well to large data sets. We have applied the package to empirical data, and demonstrated the method's ability to recover known data-generating processes by simulating data with agent-based models and correctly deriving the underlying decision models for multiple agent models and degrees of stochasticity. These applications of the package are described in a 2015 working paper by John Nay and Jonathan Gilligan: \`\`Data-driven Dynamic Decision Models''. If you use this package, cite: "Nay John and Gilligan Jonathan (2015). fsm: Estimating Finite State Machine Models. R package version 0.1. <https://github.com/JohnNay/fsm>".

This work is supported by NSF grants EAR-1416964 and EAR-1204685.

Install and load the latest release of the package from GitHub:

``` {.r}
install.packages("devtools")
devtools::install_github("JohnNay/fsm")
library(fsm)
```

Please cite the package if you use it with the text generated by:

``` {.r}
citation("fsm")
#> 
#> To cite package 'fsm' in publications use:
#> 
#>   Nay John and Gilligan Jonathan (2015). fsm: Estimating Finite
#>   State Machine Models. R package version 0.0.0.9000.
#>   https://github.com/JohnNay/fsm
#> 
#> A BibTeX entry for LaTeX users is
#> 
#>   @Manual{,
#>     title = {fsm: Estimating Finite State Machine Models},
#>     author = {Nay John and Gilligan Jonathan},
#>     year = {2015},
#>     note = {R package version 0.0.0.9000},
#>     url = {https://github.com/JohnNay/fsm},
#>   }
```

Check out the documentation for the main function of the package:

``` {.r}
?evolve_model
```

Create data and estimate model with that data:

``` {.r}
cdata <- data.frame(period = 1:5, outcome = c(1,2,1,1,1),
my.decision1 = c(1,0,1,1,1), other.decision1 = c(0,0,0,1,1))
(result <- evolve_model(cdata))
```

Use the summary method on the output of the evolve\_model function:

``` {.r}
summary(result)
```
