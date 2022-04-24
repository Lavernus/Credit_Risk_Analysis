# Credit Risk Prediction Analysis
## Overview
This analysis will be performed on credit card credit from a peer-to-peer lending services company. The client requested a model that would predict the risk of a loan.
### Purpose
Utilizing naive, random oversampling, SMOTE oversampling, Cluster Centroids undersampling, SMOTEENN combined sampling, and two ensemble algorithms: Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier, I will create six different models to predict loan risk. For each model I will calculate the balanced accuracy score and an imbalanced classification report that can be used to determine which model, if any, should be used for risk prediction.
## Results
- Naive Random Oversampling

    ![Naive.png](https://github.com/Lavernus/Credit_Risk_Analysis/blob/main/Images/Naive.png)
    - The balanced accuracy score for naive random oversampling is 0.657, the precision score is 0.01 for high risk loans, 1.00 for low risk loans, and 0.99 overall, and the recall score is 0.71 for high risk, 0.60 for low risk, and 0.60 overall.
- SMOTE Oversampling

    ![SMOTE.png](https://github.com/Lavernus/Credit_Risk_Analysis/blob/main/Images/SMOTE.png)
    - The balanced accuracy score for SMOTE oversampling is 0.654, the precision score is 0.01 for high risk loans, 1.00 for low risk loans, and 0.99 overall, and the recall score is 0.61 for high risk, 0.69 for low risk, and 0.69 overall.
- Cluster Centroids Undersampling

    ![Under.png](https://github.com/Lavernus/Credit_Risk_Analysis/blob/main/Images/Under.png)
    -The balanced accuracy score for Cluster Centroids undersampling is 0.545, the precision score is 0.01 for high risk loans, 1.00 for low risk loans, and 0.99 overall, andthe recall score is 0.69 for high risk, 0.40 for low risk, and 0.40 overall.
- SMOTEENN Combination Sampling

    ![SMOTEENN.png](https://github.com/Lavernus/Credit_Risk_Analysis/blob/main/Images/SMOTEENN.png)
    - The balanced accuracy score for SMOTEENN combination sampling is 0.679, the precision score is 0.01 for high risk loans, 1.00 for low risk loans, and 0.99 overall, and the recall score is 0.80 for high risk, 0.56 for low risk, and 0.56 overall.
- Balanced Random Forest Classifier

    ![Forest.png](https://github.com/Lavernus/Credit_Risk_Analysis/blob/main/Images/Forest.png)
    - The balanced accuracy score for Balanced Random Forest Classifier is 0.789, the precision score is 0.03 for high risk loans, 1.00 for low risk loans, and 0.99 overall, and the recall score is 0.70 for high risk, 0.87 for low risk, and 0.87 overall.
- Easy Ensemble AdaBoost Classifier

    ![Easy.png](https://github.com/Lavernus/Credit_Risk_Analysis/blob/main/Images/Easy.png)
    - The balanced accuracy score for SMOTEENN combination sampling is 0.932, the precision score is 0.09 for high risk loans, 1.00 for low risk loans, and 0.99 overall, and the recall score is 0.92 for high risk, 0.94 for low risk, and 0.94 overall.
## Summary
Of the models tested in this analysis, the one with the highest balanced accuracy score was the Easy Ensemble AdaBoost Classifier model with a score of 0.932. The rest of the models fell between 0.5 and 0.8, with the Cluster Centroids Undersampling model at the lowest with a score of 0.545.

Precision scores for low risk loans were uniformly 1.00, or 100%, across all models. The overall precision score was also the same for all models at 0.99. High risk loans had a much lower precision, however, with most models clocking in at the score 0.01. The highest score for high risk precision belonged to the Easy Ensemble AdaBoost Classifier model at 0.09.

Recall fluctuated across the models, but the best performing was undoubtedly the Easy Ensemble AdaBoost Classifier model with a score of 0.92 for high risk, 0.94 for low risk, and 0.94 overall. The worst performing was the Cluster Centroids Undersampling model with a score of 0.69 for high risk loans, 0.40 for low risk loans, and an overall score of 0.40.

### Recommendation
For the purposes of predicting loan risk I would recommend the Easy Ensemble AdaBoost Classifier model. A balanced accuracy score of 0.932 is extremely high and shows that the model is able to correctly classify loans as low or high risk almost perfectly. The precision for high risk loans is also much higher than the other models at 0.09, and the model's recall especially stands out with an overall score of 0.94. 

While the precision for high risk loans is higher than the others, it is still a meagre score suggesting that only 9% of the loans predicted as high risk are actually risky. This is acceptable, however, as it is more important for the test to be sensitive than it is to be precise. If someone is not approved for a loan because it was deemed to be high risk, while it would be unfortunate for them to be unable to aquire whatever it is they need the loan for, it would be worse if they were approved for a loan that turned out to be high risk and they found themselves in unsurmountable debt. In the first scenario they just lose what they could possibly have, in the last scenario they could lose everything they already have to debt. This means that the Easy Ensemble AdaBoost Classifier is perfect for our purposes, as the low precision for high risk loans is offset by the extremely high recall score of 0.92. 