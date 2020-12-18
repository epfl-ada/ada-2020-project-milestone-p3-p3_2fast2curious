# Creative extension proposal from a study about the impact of replacing dirt floors with cement floors on child health and adult happiness

**Publication** : Cattaneo, Matias D., Sebastian Galiani, Paul J. Gertler, Sebastian Martinez, and Rocio Titiunik. 2009. "Housing, Health, and Happiness." American Economic Journal: Economic Policy, 1 (1): 75-105.


## Reproducibility:

The notebook has already been run but in case you would like to run it the code most import missingno, lightGBM
 - `!pip install missingno`
 - `!pip install lightGBM`
Also the data has been deleted. 

# Abstract

Piso Firme is a large-scale Mexican program that replaces dirt floors with cement floors. This study aims to identify main causes of children's diseases with the help of machine learning methods and estimate the impact of Piso Firme on exposure to disease by developing an observational study. Using a set of indicators from a survey conducted in 2005 about a cohort of 6 693 individuals living in both cities targeted or not by the program, a logistic regression model was trained to estimate identify the most relevant and interpretable combination of features. Considering results from the logistic regression, an observational study was conducted and results were then compared with those from a naive study. Said results can help identify targets for the improvement of children's development and health. 

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



