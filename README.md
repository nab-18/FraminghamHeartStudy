# Framingham Heart Study Predictive Model
## Introduction

The human heart is a vital organ that has many factors that can affect its functioning. The Framingham Heart Study was conducted in Framingham, Massachusetts and is a landmark study in cardiovascular health as it considered not only multiple factors that could affect the heart, but their long-term effects and their interactions. Participant clinic data was collected during three examination periods, approximately 6 years apart, from roughly 1956 to 1968. This project aims to determine whether a patient will live or die based on the data collected in the study. Analysis of the data was conducted and three models applied to it: XGboost Classifier, Random Forest Classifier and a Logistic Regression model. We performed hyperparameter optimisation using Bayesian Hyperparameter Optimisation, with HyperOpt and evaluated the model using ROC curves and computing the area under the curves. We assessed feature importance using SHAPley explanations.

## Exploratory Data Analysis

We checked various summary statistics to familiarise ourselves with the dataset. We checked correlation among features to eliminate the possibility of high variance and this would also allow us to determine the individual effects of features later on. We assessed this correlation using SHAP values at the end as well.

![Correlation Plot](https://github.com/user-attachments/assets/09d1048c-6271-4dba-b91d-33612b4ce058)

## Hyperparameter Optimisation

Bayesian Hyperparameter Optimisation is the chosen method. It has a few advantages that are worth mentioning. It will not brute force its way through the problem as other methods would. This means that we can still get quality results, efficiently.

## Model Analysis and Visualisation

Using ROC curves, we compared the 3 models and compute their AUC's.

`XGBoost AUC: 0.812`
`Random Forest AUC: 0.798`
`Logistic Regression AUC: 0.807`

![ROC Curve](https://github.com/user-attachments/assets/8beb9ae7-18b9-4718-9569-2125de684e9e)

We used confusion matrices to determine which models were struggling with which predictions. Furthermore, SHAP values were used for feature importance.

## Analyses and Conclusion

Using the Framingham Heart Study, this project aimed to predict the outcome of a particular patient based on the recorded features. We conducted our exploratory data analysis and found that our target variable had 2 unbalanced classes. We also eliminated features that would result in data leakage or redundancy by using correlation plots. We created 3 models to compare: an XGBoost Classifier, a Random Forest Classifier and a Logistic Regression model. Bayesian Hyperparameter Optimisation was conducted using HyperOpt. Results found that the XGBoost model took the longest to optimise and the logistic regression took the shortest. The XGBoost outperformed both models by a small amount and the Logistic Regression model came second. However, noting that the dataset was not very big and the Logisitic Regression took less time to optimise, we cannot conclude that the XGBoost Classifier was a better model. The SHAPley explanations were conducted on the XGBoost model and it found that Age was the biggest factor that influenced death. In conjunction with period, the occurrence of Angina Pectoris, Myocardial Infarction, Heart Failure, and Cerebrovascular disease would be a notable factor to consider when prioritising patients. This project could have been improved by adding different models and assessing their effectiveness. Furthermore, a comprehensive review could be conducted to get a better understanding of the features and their interactions. The project could be applied to contemporary fields in numerous ways. We determined which factors affect the possibility of death and thus can focus resources and time into minimising these issues. Furthermore, patients with these issues could be prioritised to reduce their possibility of death.

## References

Barla, N. (2024) How to do Model Visualization in machine learning?, neptune.ai. Available at: https://neptune.ai/blog/visualization-in-machine-learning#:~:text=Machine%20learning%20visualization%20(ML%20visualization,through%20graphical%20or%20interactive%20means. (Accessed: 25 May 2024). 

Dataman, C.K. (2023) Explain your model with the shap values, Medium. Available at: https://medium.com/dataman-in-ai/explain-your-model-with-the-shap-values-bc36aac4de3d (Accessed: 10 June 2024). 

Hyperopt: Distributed asynchronous hyper-parameter optimization (no date) Hyperopt Documentation. Available at: http://hyperopt.github.io/hyperopt/ (Accessed: 25 June 2024). 

Jain, A. (2024) Mastering xgboost parameters tuning: A complete guide with python codes, Analytics Vidhya. Available at: https://www.analyticsvidhya.com/blog/2016/03/complete-guide-parameter-tuning-xgboost-with-codes-python/ (Accessed: 25 June 2024). 

Koehrsen, W. (2018) Hyperparameter tuning the random forest in python, Medium. Available at: https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74 (Accessed: 15 June 2024). 

Labs, D.D. (2017) Parameter tuning with Hyperopt, Medium. Available at: https://medium.com/district-data-labs/parameter-tuning-with-hyperopt-faa86acdfdce (Accessed: 20 June 2024). 

Shap (no date) Shap/SHAP: A game theoretic approach to explain the output of any machine learning model., GitHub. Available at: https://github.com/shap/shap (Accessed: 25 June 2024). 

The ‘framingham’ data set (no date) R. Available at: https://search.r-project.org/CRAN/refmans/riskCommunicator/html/framingham.html (Accessed: 25 May 2024). 
