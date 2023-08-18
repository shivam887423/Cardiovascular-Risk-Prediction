# Cardiovascular-Risk-Prediction

This project aims to predict the 10-year risk of developing coronary heart disease (CHD) using the Cardiovascular Risk Prediction dataset. The dataset contains information on 3,390 individuals with 16 predictor variables and 1 target variable. The variables represent potential demographic, behavioral, and medical risk factors.

![cardio](https://github.com/Shivam-Pandey2/Cardiovascular-Risk-Prediction/assets/119883273/23ba5da4-28e0-4727-95b5-86dcf1de621b)

# Problem Statement
The dataset is from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The classification goal is to predict whether the patient has a 10-year risk of future coronary heart disease (CHD). The dataset provides the patients’ information. It includes over 4,000 records and 15 attributes. Each attribute is a potential risk factor. There are both demographic, behavioural, and medical risk factors. Attributes includes various factors based on the mentioned three categories like sex, age, diabetes, TenYearCHD, is_smoking, etc. For this project, we have used various analysing techniques which includes Data acquisition, Data Description, Missing values imputation, Graphical Representation, Modelling, etc.

# Project Summary
The goal of this project was to use machine learning techniques to predict the 10-year risk of future coronary heart disease (CHD) in patients using data from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The dataset provided information on over 4,000 patients and included 15 attributes, each representing a potential risk factor for CHD. These attributes included demographic, behavioral, and medical risk factors.

To prepare the data for analysis, extensive preprocessing was performed to clean and transform the data. This included handling missing values using median, mode, and KNN imputation techniques, as well as identifying and removing outliers using the Interquartile Range (IQR) method. Skewed continuous variables were also transformed using log and square root transformations to reduce skewness and improve model performance.

Feature selection was performed using variance inflation factor to remove multicollinearity and a new feature called pulse pressure was created to capture the relationship between systolic and diastolic blood pressure. Redundant columns were also removed to simplify the dataset. The most important features for predicting CHD risk were identified as ‘age’, ‘sex’, ‘education’, ‘cigs_per_day’, ‘bp_meds’, ‘prevalent_stroke’, ‘prevalent_hyp’, ‘diabetes’, ‘total_cholesterol’, ‘bmi’, ‘heart_rate’, ‘glucose’, and ‘pulse_pressure’.

To handle the imbalanced nature of the dataset, the SMOTE combined with Tomek links undersampling technique was used to balance the class distribution and improve model performance. The data was also scaled using standard scalar method to ensure that all features were on the same scale.

Several machine learning models were evaluated on their performance on the primary evaluation metric of recall. After careful analysis, the Neural Network (tuned) was chosen as the final prediction model because it had the highest recall score among the models evaluated. By selecting a model with a high recall score, the goal was to correctly identify as many patients with CHD risk as possible, even if it meant having some false positives.

Overall, this project demonstrated the potential of machine learning techniques to accurately predict CHD risk in patients using data from a cardiovascular study. By carefully preprocessing and transforming the data, selecting relevant features, and choosing an appropriate model based on its performance on a relevant evaluation metric, it was possible to achieve a positive business impact by accurately predicting CHD risk in patients.

#  Dataset

**Demographic:**

• Sex: male or female ("M" or "F")

• Age: Age of the patient;(Continuous - Although the recorded ages have been truncated to whole numbers, the concept of age is continuous)

**Behavioural** 

• is smoking: whether or not the patient is a current smoker ("YES" or "NO")

• Cigs Per Day: the number of cigarettes that the person smoked on average in one day. (Can be considered continuous as one can have any number of cigarettes, even half a cigarette.)

**Medical(history)**

• BP Meds: whether or not the patient was on blood pressure medication (Nominal)

• Prevalent Stroke: whether or not the patient had previously had a stroke (Nominal)

• Prevalent Hyp: whether or not the patient was hypertensive (Nominal)

• Diabetes: whether or not the patient had diabetes (Nominal) Medical(current)

• Tot Chol: total cholesterol level (Continuous)

• Sys BP: systolic blood pressure (Continuous)

• Dia BP: diastolic blood pressure (Continuous)

• BMI: Body Mass Index (Continuous)

• Heart Rate: heart rate (Continuous - In medical research, variables such as heart rate though in fact discrete, yet are considered continuous because of large number of possible values.)

• Glucose: glucose level (Continuous) Predict variable (desired target) • 10-year risk of coronary heart disease CHD (binary: “1”, means “Yes”, “0” means “No”) - DV

Datasets: In this analysis we have used the following datasets.

Cardiovascular_risk_df: This dataframe is a created directly from the given file and since data was not very large all the attributes were included in this single dataframe and manipulated throughout the process.

# Exploratory Data Analysis

EDA Visualization is performed by using seaborn libraries with various plots like histogram, violin plot, bar plot, etc. We have used these plots for describing correlations, for relationship of sex and person who is smoking or not, other attributes and their affect on target variable CHD. Visualizations comes in handy to do Univariate-variate and multi-variate analysis.

# Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:

**Bar Plot.**

**Histogram.**

**Scatter Plot.**

**Pie Chart.**

**Line Plot.**

**Heatmap.**

**Box Plot**

# Graphs 

**Cardiovascular Risk Prediction by Age and Systolic Blood Pressure**

![image](https://github.com/Shivam-Pandey2/Cardiovascular-Risk-Prediction/assets/119883273/3496223d-c5bc-40a9-924a-4027e4b8d415)


**Distribution of Age by Ten Year CHD**

![image](https://github.com/Shivam-Pandey2/Cardiovascular-Risk-Prediction/assets/119883273/64f149dd-a9d3-4ee2-af47-36b494b0e017)

**Number of Males with vs Female suffering from heart disease**

![image](https://github.com/Shivam-Pandey2/Cardiovascular-Risk-Prediction/assets/119883273/05ec94c5-11c9-4452-8409-adaf5d2d7ae1)

# Label Encoding:

Machine Learning is performed only on numerical values, so there might be some column which do not have numerical values. Label Encoding is a popular encoding technique for handling categorical variables. In this technique, each label is assigned a unique integer based on alphabetical ordering. We performed this technique on attributes sex and is smoking.

# Feature Selection:

Feature selection or variable selection is the process of selecting a subset of relevant features or variables from the total features of a level in a data set to build machine learning algorithms.

**Advantages of selecting features:**

There are various advantages of feature selection process. These are as follows:

Improved accuracy

Simple models are easier to interpret.

Shorter training times

# Models Selection:

**Logistic Regression Model**

**k-nearest neighbor**

3)**Decision Tree**

4)**Random Forest**

**1.Logistic Regression:(With and Without Hyper-parameter Tunning)**

Logistic regression is a statistical model that in its basic form uses a logistic function to model a binary dependent variable, although many more complex extensions exist. In regression analysis, logistic regression (or logit regression) is estimating the parameters of a logistic model (a form of binary regression).

**2.K-nearest Neighbour: (With and Without Hyper-parameter Tunning)**

The k-nearest neighbors (KNN) algorithm is a simple, supervised machine learning algorithm that can be used to solve both classification and regression problems. It's easy to implement and understand, but has a major drawback of becoming significantly slows as the size of that data in use grows.

**3.Decision Tree: (With and Without Hyper-parameter Tunning)**

Decision trees help you to evaluate your options. Decision Trees are excellent tools for helping you to choose between several courses of action. They provide a highly effective structure within which you can lay out options and investigate the possible outcomes of choosing those options.

**4.Random Forest Classifier:(Ensemble technique based on bagging)**

A Random Forest is a reliable ensemble of multiple Decision Trees (or CARTs); though more popular for classification, than regression applications. Here, the individual trees are built via bagging (i.e., aggregation of bootstraps which are nothing but multiple train datasets created via sampling of records with replacement) and split using fewer features. The resulting diverse forest of uncorrelated trees exhibits reduced variance; therefore, is more robust towards change in data and carries its prediction accuracy to new data. However, the algorithm does not work well for datasets having a lot of outliers, something which needs addressing prior to the model building.

# Conclusion

**In conclusion, this project demonstrated the potential of machine learning techniques to accurately predict the 10-year risk of future coronary heart disease (CHD) in patients using data from an ongoing cardiovascular study. Key points from this project include:**

Careful data preprocessing and transformation improved the performance of machine learning models and enabled more accurate predictions.
Feature selection was important for identifying the most relevant predictors of CHD risk.
The Neural Network model (tuned) was chosen as the final prediction model due to its high recall score.
Techniques such as SMOTE combined with Tomek links undersampling and standard scalar scaling were used to handle imbalanced data and improve model performance.
This project provides a valuable example of how machine learning techniques can be applied to real-world problems to achieve positive business impact.
Overall, this project highlights the importance of careful data preparation and analysis in machine learning projects. By taking the time to clean and transform the data, select relevant features, and choose an appropriate model, it is possible to achieve accurate predictions and support decision-making in a wide range of domains.

# Challenges Faced

We have outliers in our dataset which accounts for 14% of data. So instead of discarding them we chose to impute them with median values of respective features.

We have 2 categorical features as string type which we labelled using label encoding.

We have so many features irrelevant for our model so we Adjust them like putting id feature as index and Those which have multicollinearity and values lower than variance threshold, we discarded them from our model.

Our target feature was highly Imbalanced. So, we use SMOTE to balance it before training.

Some computations were complex and had to be done correctly since wrong computations would have led to loss of data.


