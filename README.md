<img width="1050" alt="image" src="https://github.com/user-attachments/assets/a8ab9a66-2b02-455e-8c68-193fea99cefc" />

<h1 align="center">ML Regression Project For Maths Score Prediction</h1>

<h4><u>Objective :</u></h4> 
Build a machine learning model to perform <b>regression</b> based on a real dataset from Kaggle. Project done in python on jupyter notebook.

<h4><u>Notes :</u></h4> 

Train models and evaluate mainly based on `R2` parameter (above `0.8` is a good model)

# Table of Contents

- [A. Pipeline Overview](#apipeline-overview)
  - [A.1. Data Import](#a1-data-import--from-kaggle)
  - [A.2. Exploratory Data Analysis (EDA) & Data Visualization](#a2-exploratory-data-analysis-eda--data-visualization)
  - [A.3. Data Preprocessing](#a3-data-preprocessing)
  - [A.5. Model Training](#a5-model-training)
  - [A.6. Model Evaluation](#a6-model-evaluation)
  - [A.7. Model Deployment](#a7-model-deployment--not-included)
- [B. Report File extracted by ydata-profiling](#breport-file-extracted-by-ydata-profiling)
- [C. Prediction Model Summary](#c-the-file-summarizing-the-prediction-models-includes-the-adjusted-r-squared-r-squared-rmse-and-time-taken-parameters-and-prediction-execution-time-based-on-this-dataset)
  - [C.1. List of trained models sorted](#c1-this-list-of-trained-models-sorted-by-fast-execution-time-and-high-r-squared-parameter)
  - [C.2. Top 5 as horizontal bar charts](#c2-top-5-as-horizontal-bar-charts)
- [D. Results](#d-results)

# A.Pipeline-Overview
1. **Data Import** : from Kaggle
2. **Exploratory Data Analysis (EDA) & Data Visualization**  
   - Check for missing values  
   - Analyze variable distributions  
   - Compute correlation matrix
   - Create a report of dataset from ydata_profiling
3. **Data Preprocessing**  
   - Data encryption :
     - Numerical features : Standardization by StandardScaler and then using median and IQR to remove outliers to increase model performance by RobustScaler
     - Categorical Nominal feature : using OneHotEncoder
     - Categorical Ordinal features : determining the orders then using OrdinalEncoder
     - Categorical Boolean features : supposing 2 values of each series ​​are ordered (just random !) and also use OrdinalEncoder
   - Filling in missing value (Nan) by SimpleImputer
   - Train/Test split
   - (Bonus) GridSearchCV to find the best hyperparameter
5. **Model Training** 
   - Linear Regression  
   - Random Forest
   - (Bonus) LazyPredict to show performances of 30-40 differents models
6. **Model Evaluation** 
   - MAE, MSE, Coefficient of determination (R2)
7. **Model Deployment** : not included

# B.Report-File-extracted-by-ydata-profiling

![image](https://github.com/user-attachments/assets/8b530734-277d-44be-8ce5-89c389dfd86b)
![image](https://github.com/user-attachments/assets/bc6415f6-9ed7-4571-8b30-ee19fbb884c0)
![image](https://github.com/user-attachments/assets/3eb44cdd-a9ee-46e1-9c5d-36d33c8fd941)
![image](https://github.com/user-attachments/assets/0d44b96d-9dc5-466e-ac08-cdf55d544ed7)
![image](https://github.com/user-attachments/assets/766dd712-29f6-43dd-b566-cd155b258f0b)
![image](https://github.com/user-attachments/assets/71c7af3a-d19f-4f6a-a0dd-9585e8cc618d)
![image](https://github.com/user-attachments/assets/7a3406c6-5b18-4b37-b47d-15f64a024d0d)
![image](https://github.com/user-attachments/assets/d825d4e4-0f04-4934-afb4-715f8efa6254)
![image](https://github.com/user-attachments/assets/c862e85b-3a89-4e1f-a425-d79f23d46928)
![image](https://github.com/user-attachments/assets/d9e15055-49bf-455e-b2d7-7c716b51ac9c)
![image](https://github.com/user-attachments/assets/2036f61a-a0d8-40cc-850d-3941c0d59e0a)



# C. The file summarizing the prediction models includes the Adjusted R-Squared, R-Squared, RMSE and Time Taken parameters and prediction execution time based on this dataset. 

#### C.1. This list of trained models sorted by fast execution time and high R-Squared parameter

![image](https://github.com/user-attachments/assets/56243b44-063f-4b93-92b3-c8aa9da7dccf)

#### C.2. Top 5 as horizontal bar charts

![image](https://github.com/user-attachments/assets/e8390853-11c4-4b6e-9ec2-1f2b40524920)


# D. Results
- All models were trained and evaluated to identify the best-performing one for this regression task.
- Reusability on other datasets thanks to calling the pickle library to store the models.







