# Heart Disease Classification

### Introduction
In this analysis, I examine the heart disease dataset to predict whether a patient has a heart disease or not. Data comes from Cleveland Heart Disease dataset from the UCI Repository.

### Dictionary

Age: displays the age of the individual.

Sex: displays the gender of the individual using the following format :
1 = male
0 = female

Chest-pain type: displays the type of chest-pain experienced by the individual using the following format :
1 = typical angina
2 = atypical angina
3 = non — anginal pain
4 = asymptotic

Resting Blood Pressure: displays the resting blood pressure value of an individual in mmHg (unit)

Serum Cholestrol: displays the serum cholesterol in mg/dl (unit)

Fasting Blood Sugar: compares the fasting blood sugar value of an individual with 120mg/dl.

If fasting blood sugar > 120mg/dl then : 1 (true)
else : 0 (false)

Resting ECG : displays resting electrocardiographic results
0 = normal
1 = having ST-T wave abnormality
2 = left ventricular hyperthrophy

Max heart rate achieved : displays the max heart rate achieved by an individual.

Exercise induced angina :
1 = yes
0 = no

ST depression induced by exercise relative to rest: displays the value which is an integer or float.

Peak exercise ST segment :
1 = upsloping
2 = flat
3 = downsloping

Number of major vessels (0–3) colored by flourosopy : displays the value as integer or float.

Thal : displays the thalassemia :
3 = normal
6 = fixed defect
7 = reversible defect

Diagnosis of heart disease : Displays whether the individual is suffering from heart disease or not :
0 = absence
1, 2, 3, 4 = present.

### Methodology
As part of data preprocessing, I examined for null and missing values which was not a point of concern with this data set. The data set had already gone through some filtering and cleaning so the data hygine was in a good shape.
As a major part of data preprocessing, I decided to dummify categorical/ordinal variables, especically since not much information was provided regarding ordinal variables.

### Modeling
I experimented with the following classifiers. It's worth noting that for all the models below, I used Pipeline to scale when appropriate and GridSearch to tune hyperparameters for optial performance.

- Logistic Regression
-  KNN
-  Random Forest
-  SVM
-  XGBoost

### Evaluation
As part of my model performance evaluation, I used two specific metrics. Accuracy and Recall (sensitivity). Accuracy score is a good indication whether the model did a good job of predicting right target variables (1 or 0) and recall score is a good indication whether the model is handling Type II errors (false negatives) well. Given this model involves predicting a serious medical condition, I paid a close attention on recall score.

### Summary
KNN and XGBoost performed extremely well. Both models scored 100% accuracy scores on both training and testing data. Both models also did not have any misclassifications which I found to be promising and impressive. One downside was that both models lacked any room for interpretability. If interpretability is a big factor, I recommend applying the Logistic Regression despite its performance measured by accuracy and sensitivity won't' be as high as with KNN and XGBoost.



