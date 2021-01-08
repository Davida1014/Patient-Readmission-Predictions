# Patient Readmission Predictions
![istockphoto-932038072-612x612](https://github.com/Davida1014/Patient-Readmission-Predictions/blob/master/Images/istockphoto-932038072-612x612.jpg?raw=true)

Elliot Macy, Davida Rosenstrauch

# Overview, Business Problem
This project seeks to create a model that classifies whether a diabetes patient in a given hospital encounter is likely to be readmitted to the hospital within 30 days of discharge. This information will help insurance companies determine individual patients' risk of returning in the hospital in this time period.

# Data, Methods
This dataset represents 101,000 hospital encounters of approximately 71,000 individual patients, across 130 US hospitals, and recorded over the 10-year period between 1999 and 2008. It includes over 50 features representing patient and hospital outcomes. Information was extracted from the database for encounters that satisfied the following criteria:
1. It is an inpatient encounter (a hospital admission).
2. It is a diabetic encounter, that is, one during which any kind of diabetes was entered to the system as a diagnosis.
3. The length of stay was at least 1 day and at most 14 days.
4. Laboratory tests were performed during the encounter.
5. Medications were administered during the encounter.

The data contains such attributes as patient number, race, gender, age, admission type, time in hospital, medical specialty of admitting physician, number of lab test performed, HbA1c test result, diagnosis, number of medication, diabetic medications, number of outpatient, inpatient, and emergency visits in the year before the hospitalization, etc. 

The dataset suffers from lack of class separation, presenting a challenge for generating predictions.

Given a class imbalance of approximately 90%-to-10% between target variables, undersampling was performed and models were conducted on a dataset of 22,714 hospital encounters.

Three classification models were performed to determine best fit: a decision tree, random forest, and XGBoost. Accuracy, precision, recall, and F1 scores were analyzed to determine the best-fit model, with an emphasis on accuracy and recall in an effort to minimize false predictions of no readmittance.

# Results
Of the three models, the XGBoost model most accurately predicted readmission, as determined via accuracy and recall. Below are confusion matrices for each model, which evidence this. Its test scoring metrics are as follows:
1. Accuracy: 62.36%
2. Recall: 62.12%
3. Precision: 62.78%
4. F1: 62.45%

Below are confusion matrices from each of the three models. As shown, the random forest and XGBoost models were significantly more accurate than the decision tree model. The XGBoost model was slighly more accurate than the random forest.

Decision Tree:

![dt_confusion](https://github.com/Davida1014/Patient-Readmission-Predictions/blob/master/Images/dt_confusion.png?raw=true)

Random Forest:

![rf_confusion](https://github.com/Davida1014/Patient-Readmission-Predictions/blob/master/Images/rf_confusion.png?raw=true)

XGBoost:

![xgb_confusion](https://github.com/Davida1014/Patient-Readmission-Predictions/blob/master/Images/xgb_confusion.png?raw=true)


Of the features included in this most successful model, number_inpatient, discharge_disposition_id, total_hosp_visits, and time_in_hospital held the most predictive power. This is outlined in the graph below, which measures feature importance.

![xgb_features](https://github.com/Davida1014/Patient-Readmission-Predictions/blob/master/Images/xgb_features.png?raw=true)

# Recommendations, Next Steps
Based on these findings, we recommend insurance companies look to diabetes patients' number of inpatient admissions over the previous year, discharge disposition id, and total number of hospital visits in the previous year to predict likelihood of hospital readmission within 30 days. Opportunites for further work include:
1. Creating a multi-class classification model to predict likelihood of hospital readmission at different intervals above 30 days.
2. Incorporating patient weight data, which was omitted here due to lack of data.
3. Conducting more recent research as modern medical innovation and technology may yield different results.
4. Using neural networks to improve model accuracy and recall.

# Summary
An XGBoost model successfully predicted hospital readmission for diabetes patients with 62.36% accuracy and 62.12% recall for 22,714 hospital encounters recorded over 10 years. Of the features used to build this model, number of inpatient admissions over the previous year, discharge disposition id, and total number of hospital visits in the previous year held the most predictive power. We recommend insurance companies, hospitals, and medical professionals look to these features when predicting likelihood of readmission for diabetes patients.

# Source
This data was accessed via the UC Irivine Machine Learning Repository via the following link: https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008
