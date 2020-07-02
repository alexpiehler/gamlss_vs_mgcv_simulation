# Code for the simulation study: `gamlss` vs. `mgcv` with zero-inflated Poisson data
This is the repository for a simulation study in which the performance of the R packages `gamlss` (Rigby et al. 2005) and `mgcv` (Wood et al. 2016) are compared for location-scale modeling with zero-inflated Poisson data. In particular the way algorithms, which estimate the smoothing parameters of the spline-functions, are compared.  This simulation study extends the work of Wood et al. (2016) by not only modeling the rate of the zero-inflated Poisson distribution through non-linear functions of covariates but also explicitly modeling the probability of zero-inflation through non-linear functions of covariates. 

It is found that the algorithm for estimating smoothing parameters in the packaged `mgcv` outperforms the algorithm `gamlss` in speed and convergence rate. While the algorithm in the `gamlss` package is less stable, especially for low mean and highly dispersed count data, it on average yields comparable results to the algorithm in the `mgcv` package.

________________________
Rigby, R. A. & Stasinopoulos, D. M. (2005), _Generalized additive models for location, scale and shape_, Journal of the Royal Statistical Society 54(3), 507-554.

Wood, S. N., Pya, N. & Säfken, B. (2016), _Smoothing parameter and model selection for general smooth models_, Journal of the American Statistical Association 111(516), 1548{1563.
