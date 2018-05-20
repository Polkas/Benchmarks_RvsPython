# Benchmarks R vs Python

Using RStudio and the reticulate package to benchmark important algorithms across R and Python environments

[**reticulate**](http://blog.rstudio.com/2018/03/26/reticulate-r-interface-to-python/)

Environment: MRO 3.4.4 i7 6700HQ 24G DDR4 2133

Hypothesis: There is no significant gap in an algorithms performance between R and Python environments.

*Algebra operations, OLS and in development phase RandomForest,random numbers generators (Mersenne-Twister, ...), NN and Xgb*

Proc usage was calculated by R function `microbenchmark::get_nanotime` and Python method `time.clock`

### Algebra - X'X

X'X takes around mn^2 flops ( the 2 power were reduced during last years but it will be always exponential).  
So time growing linear with additional rows and quadratic with additional columns.

![](./png/Algebra_XX.png)

### OLS

OLS consists of solving linear systems with usage of cholesky,QR or LU matrix decomposition

Example under QR decomposition:

![](./png/OLS.png)

### Random Forest

### NN

### XGB