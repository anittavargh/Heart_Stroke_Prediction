# heart_stroke_prediction

To develop a predictive model that can identify individuals at risk of suffering a heart stroke. 

This predictive model will use various patient characteristics and health-related factors to assess the likelihood of a heart stroke.

Data source: https://www.kaggle.com/datasets/lirilkumaramal/heart-stroke

Data Preprocessing: Filtered relevant features and filled the missing values

Exploratory Data Analysis (EDA) is a critical initial step in the data analysis process that involves examining and summarizing the main characteristics, patterns, and trends within a dataset.

Used get_dummies to change categorical values

Used RandomOverSampler to oversample the minority class(getting stroke)
----------------------------------------------------------------

After adjusting probabilities

Random forest 

 		precision    recall  f1-score   support
	
	1       0.10      0.69      0.18        35

Accuracy - 0.7867
----------------------------------------------------------------
XGBoost classifier

 		precision    recall  f1-score   support

           1       0.11      0.71      0.19        35

Accuracy - 0.7945
----------------------------------------------------------------
k-Nearest Neighbors

 		precision    recall  f1-score   support

           1       0.06      0.23      0.10        35

Accuracy 0.8601
--------------------------------------------------------------
Logistic Regression

    		precision    recall  f1-score   support

           1       0.10      0.83      0.17        35

Accuracy 0.7309
----------------------------------------------------------------

Neural Networks

 		precision    recall  f1-score   support

           1       0.08      0.23      0.12        35

Accuracy 0.8885
--------------------------------------------------------------------

By analysing the results we can see that recall(tp/tp+fn) is highest for logistic regression where we can minimise the number of false negatives which is critcal for this model as we are predicting stroke and we dont want to predict that a person who is susceptible for stroke is predicted wrongly. So it is important to have a higher recall and hence Logistic regression is the best model in use case.
