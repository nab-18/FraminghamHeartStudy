# FraminghamHeartStudy
## Introduction

The human heart is a vital organ that has many factors that can affect its functioning. The Framingham Heart Study was conducted in Framingham, Massachusetts and is a landmark study in cardiovascular health as it considered not only multiple factors that could affect the heart, but their long-term effects and their interactions. Participant clinic data was collected during three examination periods, approximately 6 years apart, from roughly 1956 to 1968. This project aims to determine whether a patient will live or die based on the data collected in the study. Analysis of the data was conducted and three models applied to it: XGboost Classifier, Random Forest Classifier and a Logistic Regression model. We performed hyperparameter optimisation using Bayesian Hyperparameter Optimisation, with HyperOpt and evaluated the model using ROC curves and computing the area under the curves. We assessed feature importance using SHAPley explanations.

## Exploratroy Data Analysis

We checked various summary statistics to familiarise ourselves with the dataset. We checked correlation among features to eliminate the possibility of high variance and this would also allow us to determine the individual effects of features later on. We assessed this correlation using SHAP values at the end as well.
