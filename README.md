
# RobustPolytomousRegression

This repository provides **R** routines which allow to perform robust polytomous regression. The different methods are detailed in [*Robust polytomous regression*, 2022](https://www.sciencedirect.com/science/article/pii/S016794732200144X). <br>
**R** code is also provided to reproduce the different simulations and figures of this papaer.

## Routines for robust polytomous regression

- sources.R :	loads necessary libraries and scripts to perform robust polytomous estimation
- common_functions.R : contains functions used by other scripts (executed by sources.R)
- ML.R : contains functions to do maximum likelihood estimation (executed by sources.R)
- MDPD.R : contains functions to do minimum density power divergence estimation described in [*New robust statistical procedures for the polytomous logistic regression models*, 2018](https://onlinelibrary.wiley.com/doi/abs/10.1111/biom.12890) (executed by sources.R)
- RGLM.R : contains functions to do robust estimation extending robust GLM setup (executed by sources.R)
- OBR_CFC.R : contains functions to do optimally B-robust conditionnaly fisher consistent estimation (executed by sources.R)
- tuning.R : contains functions to tune robustness tuning parameter (executed by sources.R)

## Reproduce results from [*Robust polytomous regression*, 2022](https://www.sciencedirect.com/science/article/pii/S016794732200144X)

### Simulations

- simulation_estimation.R : simulate clean and outlier-contaminated datasets to compare different polytomous regression estimators
- simulation_score_test_alternative.R : simulate, under alternative hypothesis, clean and outlier-contaminated datasets and perform score-tests associated with different estimators
- simulation_score_test_null.R : simulate, under null hypothesis, clean and outlier-contaminated datasets and perform score-tests associated with different estimators
- simulation_wald_test_alternative.R : simulate, under alternative hypothesis, clean and outlier-contaminated datasets and perform Wald-tests associated with different estimators
- simulation_wald_test_null.R : simulate,  under null hypothesis, clean and outlier-contaminated datasets and perform Wald-tests associated with different estimators

### Cross validation

- cross_validation.R : performs 10-fold cross on two datasets
- cross_validation_mammo.R : performs 10-fold cross on the *mammography* dataset
- cross_validation_vertebral.R : performs 10-fold cross on the *vertebral* dataset

### Figures

- plot_IF.R : plot the influence function of 4 polytomous regression estimators
- plot_boxplots_simulation_estimations.R : plot boxplots of 
- plot_cross_validation.R : plot boxplots of output of `cross_validation.R`
- plot_simulation_estimation_v2.R : plot the efficiency of different estimators under different levels of contamination (uses the ouput of `simulation_estimation.R`)
- plot_simulation_test.R : plot the power and levels of the Wald and score tests associated with different estimators under different levels of contamination (uses the ouput of `simulation_estimation_test.R`)
- plot_weights.R : plot the weighting functions of RGLM and MDPD estimators 
