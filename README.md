# Creative extension proposal from a study about the impact of replacing dirt floors with cement floors on child health and adult happiness

**Publication** : Cattaneo, Matias D., Sebastian Galiani, Paul J. Gertler, Sebastian Martinez, and Rocio Titiunik. 2009. "Housing, Health, and Happiness." American Economic Journal: Economic Policy, 1 (1): 75-105.


# Abstract

The original publication, mentioned above, from which this study is derived, focused on the impact of a large-scale Mexican program that replaces dirt floors with cement floors on the health of children and happiness of adults. Here we proposed to estimate the importance of Piso Firme on children's health. The first part will be focused on using Machine Learning algorithms to identify features that are important for children's health : we will define a target (general health status) using the different outcomes about health already present in the data and then, using feature selection methods to come up with a simple and interpretable model for children's health. The rest will be about conducting an observational study using selected features as potential confounders. 

## Research questions

 1. What are the main causes of disease ? 
 2. In which ways Piso Firme can explain these diseases ? 

## Proposed dataset

The [original dataset](https://www.openicpsr.org/openicpsr/project/114542/version/V1/view) from the article.

## Methods

 1. Imputation of the missing values with a K-Nearest Neighbor algorithm. 
 2. Construction of the target for machine learning algorithms. 
 3. Feature selection : 
                                    - recursive feature selection
                                    - Pearson's correlation
                                    - Chi-2
                                    - Lasso regularization
4. Construction of a logistic regression model based on selected features. 
5. Outcome analysis (without matching).
6. Calculate propensity scores, based on selected features. 
7. Find the best matching using the propensity scores (bipartite graph). 
8. Balance checking.
9. Outcome analysis (with matching).
10. Sensitivity analysis (if time allows)

## Proposed timeline

**Week 1** : generation of the logistic regression model, feature selection, feature engineering and first outcome analysis. Generate propensity scores.

**Week 2** : Generation balanced samples using matching, second outcome analysis, and sensitivity analysis

## Organization within the team

**Elia** : preparation of the logistic regression model (feature selection, feature engineering), interpreting results.

**Hugo** : preparation of the logistic regression model (feature selection, feature engineering), interpreting results.

**Pierre** : generation of propensity scores and matching, interpreting results. Sensitivity analysis. 

## Questions for the TAs

