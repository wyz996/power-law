# power-law
Matlab code for fitting power law distribution
**********************************************************************************
randht.m 
Random number generators.
This function generates continuous values randomly distributed according to one of the five distributions discussed in the article (power law, exponential, log-normal, stretched exponential, and power law with cutoff). Usage information is included in the file; type 'help randht' at the Matlab prompt for more information.
		
**********************************************************************************
plfit.m
Fitting a power law distribution.
This function implements both the discrete and continuous maximum likelihood estimators for fitting the power-law distribution to data, along with the goodness-of-fit based approach to estimating the lower cutoff for the scaling region. Usage information is included in the file; type 'help plfit' at the Matlab prompt for more information.
**********************************************************************************
plplot.m
Visualizing the fitted distribution.
After several requests, I've written this function, which plots (on log-log axes) the empirical distribution along with the fitted power-law distribution. Usage information is included in the file; type 'help plplot' at the Matlab prompt for more information
**********************************************************************************
plvar.m
Estimating uncertainty in the fitted parameters.
This function implements the nonparametric approach for estimating the uncertainty in the estimated parameters for the power-law fit found by the plfit function. It too implements both continuous and discrete versions. Usage information is included in the file; type 'help plvar' at the Matlab prompt for more information.
**********************************************************************************
plpva.m
parplpva2.m(Matlab, by Casper Peterson, uses Parallel Toolbox)
Calculating p-value for fitted power-law model.
This function implements the Kolmogorov-Smirnov test (which computes a p-value for the estimated power-law fit to the data) for the power-law model. As above, it too implements both continuous and discrete versions of the test. Usage information is included in the file; type 'help plpva' at the Matlab prompt for more information.
**********************************************************************************
deta.m
zeta.m
Riemann Zeta function 
The discrete estimator needs to calculate the Hurwitz Zeta function for normalization. Matlab includes this function in the Symbolic Math Toolbox (but be warned that their implementation becomes unstable for large alpha and xmin, e.g., alpha>7 with xmin>150). There are also free versions available if you don't have this toolbox. For instance, Paul Godfrey's special functions library (via Matlab Central File Exchange) gives one, which we mirror here (note, you need both these files; tip to Will Tracy).
**********************************************************************************
**********************************************************************************

http://tuvalu.santafe.edu/~aaronc/powerlaws/

Journal References
A. Clauset, C.R. Shalizi, and M.E.J. Newman, "Power-law distributions in empirical data" SIAM Review 51(4), 661-703 (2009). (arXiv:0706.1062, doi:10.1137/070710111)

Y. Virkar and A. Clauset, Power-law distributions in binned empirical data. Annals of Applied Statistics 8(1), 89 - 119 (2014). (arXiv:1208.3524; get the code) 
