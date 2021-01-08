# Patient Readmission Predictions
![istockphoto-932038072-612x612](https://github.com/Davida1014/Patient-Readmission-Predictions/blob/master/Images/istockphoto-932038072-612x612.jpg?raw=true)

# Overview, Business Problem
This project seeks to create a model that classifies whether a diabetes patient in a given hospital encounter is likely to be readmitted to the hospital within 30 days of discharge. This information will help insurance companies determine individual patients' risk of returning in the hospital in this time period.

# Data and Methods
This dataset represents 101,000 hospital encounters of approximately 71,000 individual patients, across 130 US hospitals, and recorded over the 10-year period between 1999 and 2008. It includes over 50 features representing patient and hospital outcomes. Information was extracted from the database for encounters that satisfied the following criteria.
1. It is an inpatient encounter (a hospital admission).
2. It is a diabetic encounter, that is, one during which any kind of diabetes was entered to the system as a diagnosis.
3. The length of stay was at least 1 day and at most 14 days.
4. Laboratory tests were performed during the encounter.
5. Medications were administered during the encounter.

The data contains such attributes as patient number, race, gender, age, admission type, time in hospital, medical specialty of admitting physician, number of lab test performed, HbA1c test result, diagnosis, number of medication, diabetic medications, number of outpatient, inpatient, and emergency visits in the year before the hospitalization, etc.

Given a class imbalance of approximately 90%-to-10% between target variables, undersampling was performed and models were conducted on a dataset of 22,714 hospital encounters. Four classification models were performed to determine best fit: a decision tree, random forest, XG boost, and logistic regression. Accuracy, precision, recall, and F1 scores were analyzed to determine the best-fit model, with an emphasis on accuracy and recall in an effort to minimize false predictions of no readmittance.

# Results
Of the four models, the XXX model most accurately predicted readmission. Below are confusion matrices for each model, which evidence this. Its scoring metrics are as follows:
Accuracy:
Precision:
Recall:
F1:

[INSERT ALL MODEL CONFUSION MATRICES]

Of the features included in this most successful model, XXX, XXX, XXX, and XXX held the most predictive power. This is outlined in the graph below, which measures feature importance.

[INSERT FEATURE IMPORTANCE GRAPH FOR BEST-FIT MODEL]

# Recommendations, Next Steps
Based on these findings, we recommend insurance companies look to diabetes patients' XXX, XXX, XXX, and XXX to predict likelihood of hospital readmission within 30 days. Opportunites for further work include:
1. Creating a multi-class classification model to predict likelihood of hospital readmission at different intervals above 30 days.
2. Incorporating patient weight data, which was omitted here due to lack of data.
3. Conducing more recent research as modern medical innovation and technology may yield different results.

# Summary
A XXX model successfully predicted hospital readmission for diabetes patients with XX% accuracy for 22,714 hospital encounters recorded over 10 years. Of the features used to build this model, XXX, XXX, XXX, and XXX held the most predictive power. We recommend insurance companies look to these features when predicting likelihood of readmission for diabetes patients.
