# Credit_Risk_Analysis

Overview

This challenge was to evaluate machine learning models to determine the best option for predicting credit risk. Credit Risk has an inherently unbalanced classification problem; hence, numerous techniques are employed to evaluate and train models with unbalanced classes. 

The machine learning models used are RandomOverSampler, SMOTE algorithms to oversample the dataset and ClusterCentroids algorithm to undersample the dataset. SMOTEENN algorithm will be utilized to over and under-sample. Thereafter we will compare EasyEnsembleClassifier both BalanacedRandomForestClassfier to predict credit risk and then assess the performance of these models. 

To execute these objectives, we will apply different unbanlanced machine learning models and compare the results. This will be executed through observing variables, view the count of the target classes, train the logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix and then generate a classification report. 

Results 

Random Oversampling 

This method handles class imbalances by duplicating the data in the minor class. For this dataset the minor class represents the high-risk loan applications and the major class the low-risk applications. 

<img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/205422022-9e8fc8fc-69bc-442f-9916-065b14ec7d97.png">

<img width="386" alt="image" src="https://user-images.githubusercontent.com/109915684/205422030-c14ae6a7-4db3-47c1-905c-307b54cebde7.png">

The Balanced Accuracy Score: 0.657

The precision for the low-risk loans was 1.00 and the precision for the high-risk loans was very low at 0.01.

The recall values for the high-risk loans were 0.71 and low risk was 0.60.

SMOTE Oversampling

This model matches the size of the major class with the minor class dataset. This is done by interpolating data from k-nearest neighbors rather than duplicating data like the Random Oversampling model. 

 <img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/205422046-fb8b5e34-bdaf-4b9c-8551-b329c58de115.png">

<img width="355" alt="image" src="https://user-images.githubusercontent.com/109915684/205422051-2ba3e7d1-0a90-4333-9579-a8b9c04a90c8.png">

The Balanced Accuracy Score was very close to that in Random Oversampling at 0.661. 

The precision values were the same as in the Random Oversampling with low-risk loans at 1.00 and high-risk loans at 0.01.

The recall values were 0.69 and 0.63 for low-risk and high-risk loans respectively.   

Undersampling

This model only employs existing data in the dataset rather than creating duplicates like the above models. But this approach may have a limitation of removing some data to ensure that the dataset is even. 

<img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/205422055-40c488a8-370a-49a1-afc9-06b27716e03e.png">

 <img width="401" alt="image" src="https://user-images.githubusercontent.com/109915684/205422067-69688573-a0f2-4694-8a4b-7a9ac3d1441c.png">
 
The Balanced Accuracy Score was 0.544 this was the lowest in comparison to the other models. 

The precision values were similar to SMOTE Oversampling and Random Oversampling at 0.01 for high-risk and 1.00 for low-risk. 

The recall values were 0.69 for high-risk and 0.40 for low-risk.

Combination (SMOTEENN) Sampling

As the name suggest this model includes both over and under sampling methods 

<img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/205422077-1803b3da-3888-4a07-bd92-f90a3fbdb7d2.png">

 <img width="418" alt="image" src="https://user-images.githubusercontent.com/109915684/205422086-bf0acb9d-694c-440d-90f5-051f9ddcf339.png">

The Balanced Accuracy Score was 0.644. 

The precision values were the same as all other models for both the low-risk and the high-risk.

The recall values were 0.71 and 0.58 for low-risk and high-risk respectively. 

Balanced Random Forest Classifier 

This model uses a mix of classification and regression technique to address imbalance data.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/205422105-76ae2e86-9854-40a5-896a-0bca8a65be99.png">

<img width="377" alt="image" src="https://user-images.githubusercontent.com/109915684/205422116-065b3247-4798-4f24-9964-08b27ca41c1a.png">

The Balanced Accuracy Score was 0.788

The precision for high-risk was 0.03 and low-risk was 1.00

The recall values were 0.70 and 0.87 for high-risk and low risk respectively.

Easy Ensemble AdaBoost Classifier

 <img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/205422123-944eb120-072a-4c6a-8582-1ba29cbafe03.png">

<img width="389" alt="image" src="https://user-images.githubusercontent.com/109915684/205422128-393bca59-8ed5-4d1b-8439-f2c2be28dd97.png"> 

The Balanced Accuracy Score was 0.931

The precision for high-risk was the highest thus far at 0.09 while low-risk remained constant with the other models at 1.00. 

The recall values were also the highest thus far for both high risk and low-risk at 0.92 and 0.94 respectively. 

Summary and Analysis

Balanced Accuracy Score 

This reflects the ratio of accuracy or true prdictions in the model. The Balanced Accuracy Scores ranged between 0.544 and 0.788 across all models except for the Easy Ensemble AdaBoost Classifier where it was 0.931. 

Precision 

This element defines the reliability of the model when a positive classification is made. Hence, a low precision value means that there are a large number of positive values in the results. The precision values were typically the same for all models with 0.01 for low-risk and 1.00 for high- risk except Balanced Random Forest Classifier, 0.03 for low-risk and 1.00 for high risk and the Easy Ensemble model where it was 0.09 for low-risk and 1.00 for high risk. 

Recall

This defines the ability of the model to identify the positive samples. Therefore, a low recall represents a large number of false negatives. For the models observed the recall values were very erratic between the different models ranging between ~ 0.63 and 0.71 for high-risk applications and 0.40 and 0.87 for low-risk. However, Easy Ensemble had the highest at 0.92 for high-risk and 0.94 for low risk. 

Conclusions and Recommendations 

Undersampling performed the poorest, even though in range to some of the models when observing some of the variables. For the Precision values and the Recall values it was approximate to the other models. Overall though it was the ineptest for predicting credit risk in this dataset. The Balanced Accuracy Score, 0.544 was the lowest in relation to the other models. Hence, this model would not be the best fit for predicting risks associated with the loan applications.  


EasyEnsemble model was one of the best predictors because the algorithm aggregates all results. The Balanced Accuracy score was 0.931, the highest of all models and best for inspiring confidence in the model’s ability to determine high-risk credit applications.  The Precision for Low Risk was 1.00 and the of 0.09 for high-risk, somewhat of a deterrent for this model.  The best recall options were also in this model with 0.92 and 0.94 for low-risk and high-risk respectively. 

The original dataset seems heavily imbalanced and skewed. Hence, for best results a bigger dataset would provide more accurate results. 
