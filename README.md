# Credit_Risk_Analysis

## Overview of Analysis
The purpose of this analysis was to apply a variety of supervised machine learning models to see how they fared in predicting credit risk and whether any should be preferred considering the inherently unbalanced classification problem of this investigation.

* NOTE: In this repository, please reference .ipynb files with "_FINAL" in the name.

## Results
- The Random Oversampling model set the bar with an accuracy score of ~67%.

![image1_RandomOversampling](/image1_RandomOversampling.png)

- The SMOTE method was less effective - it correctly classified ~64% of credit risks.

![image2_SMOTEOversampling](/image2_SMOTEOversampling.png)

- Undersampling was fairly comparable to the two but most-closely resembled SMOTE - it too came in around 64%.

![image3_Undersampling](/image3_Undersampling.png)

- The SMOTEEN method was the first to veer significantly from the mid-60s in terms of accuracy score - it failed to correctly classify even 55% of tests (though it is the most sensitive of the first four models, which is valuable in a credit risk data set).

![image4_SMOTEEN](/image4_SMOTEEN.png)

- The ensemble learners both fared far better. The Balanced Random Forest yielded an accuracy score >99.9% and correctly identified all 101 true positives!

![image5_RandomForest](/image5_RandomForest.png)

- Though it could scarcely outdo the Balanced Random Forest, the Ensemble Boost also identified all 101 true positives and managed an accuracy score of 100%!

![image6_BoostClassifier](/image6_BoostClassifier.png)

## Summary
After testing a half dozen separate machine learning models on our credit risk data, it is clear that the ensemble learners are the way to go. Not only was each far more accurate than any standard oversampled or undersampled evaluation, but also they didn't miss identifying a single risky credit loan, a key measure for this problem. That said, any model that comes across as that accurate should inspire skepticism so further investigation to determine whether or not a mistake was made should be undertaken. Assuming further tests sign off on the validity of the model, either ensemble learner would be a great tool for a lender.
