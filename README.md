# Cardiovascular-Risk-Prediction


Cardiovascular Risk Prediction dataset provides the patients' information. The dataset contains information on 3,390 individuals with 16 predictor variables and 1 target variable. Each variable (attribute) is a potential risk factor. There are demographic, behavioral, and medical risk factors. We were tasked to predict the 10-year risk of developing coronary heart disease (CHD).


After understanding the data and getting variables, we first gathered and cleaned the data, handled the null values by checking the distribution and outliers in the data after that we have also typecasted the needed features into required format by type casting in order to visualize them properly. We performed indepth EDA and plotted different types of graphs by separating them into univariate, bivariate and multivariate categories as a result, We came accross some meaningful insights that helped us to make future decisions of ML model pipeline. Then further on, using feature engineering and data preprocessing we have extracted new features like pulse_pressure and glucose_diabetes with the help of some features which are not directly impacting to tenYearCHD. We also tried to get some impacting features by removing multicollinearity within the independent variables with the help of various inflation factor(VIF). In this dataset we have not handled outliers as removing them could potentially lead to a loss of important information and biased results. Also, we noticed that some of the features were categorical in nature and ML model can not understand the language of alphabets(strings).So, we have encoded them into numericals using BINARY LABEL ENCODING .



Overall, while building a machine learning model on Cardiovascular risk prediction data, we applied combination of data processing, machine learning techniques, and model evaluation skills. It was a challenging task and we faced some failures as well but with the right approach and knowledge, we successfully created a model that can accurately predict a patient that can be infected with CHD in future.

