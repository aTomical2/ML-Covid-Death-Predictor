# ML-Covid-Death-Predictor

## Overview

This project analyses and predicts patient outcomes using a dataset of medical and demographic features. he dataset originates from CDC’s Covid-19 database and was processed to predict the target variable death_yn (Yes/No). The repository demonstrates a complete data science workflow, from preprocessing and exploratory data analysis to implementing and evaluating machine learning models.

## Features

- **Data Preprocessing**:
  - Management of categorical and numerical variables.
  - Conversion of data types for compatibility with models.
  - Generation of frequency tables for dataset summarisation.
  
- **Exploratory Data Analysis (EDA)**:
  - Visualisation of feature distributions and mortality rates.
  - Descriptive statistics for demographic and medical variables.

- **Machine Learning Models**:
  - Linear Regression
  - Logistic Regression
  - Random Forest Classifier

- **Model Evaluation**:
  - Performance metrics such as accuracy, precision, recall, and F1 scores.
  - Cross-validation for robust model assessment.

## Files

  - new_features_df1.csv: Processed dataset containing patient records and features for analysis.
  - ML_Notebook.ipynb: Jupyter Notebook with detailed analysis and implementation.

### **Step 1: Install Prerequisites**  

To run the notebook, you need the following Python libraries installed:
  - pandas
  - matplotlib
  - scikit-learn
  - numpy
  - scipy

Install the dependencies using pip:
pip install pandas matplotlib scikit-learn numpy scipy

### **Step 2: Dataset Overview**  
The dataset contains 50,000 entries randomly sampled from the CDC's database, reduced to 11 independent variables and one target variable after cleaning. Key features include:
  - Demographic information: age_group, sex, race, ethnicity.
  - Medical details: hosp_yn (hospitalisation status).
  - Geographic and political information: county_frequency_size, party.

### **Step 3: Data Preprocessing**
Features such as case_month and Profile were removed due to multicollinearity.
Categorical variables were encoded for model compatibility.
Frequency tables were generated to summarise feature distributions.

### **Step 4: Exploratory Data Analysis (EDA)**
Summary statistics and visualisations were created for key features, highlighting:
Mortality (death_yn): 8,390 deaths vs. 31,557 survivals.
hosp_yn: 6,379 (Yes), 33,568 (No) (Indicating strong correlation with mortality)
Party affiliations: 26,784 (Democrats), 13,163 (Republicans).

### **Step 5: Model Development**
Data split: 70% for training (27,962 rows) and 30% for testing (11,985 rows).
Algorithms employed include:
  - Linear Regression
  - Logistic Regression
  - Random Forest Classifier

Pipelines for data preprocessing, including scaling and encoding, were integrated.

### **Step 6: Model Evaluation**
Metrics such as accuracy, precision, recall, and F1 scores were calculated. These metrics help evaluate the models' performance on classifying mortality (death_yn).

Key Insights

Mortality Correlations: The data showed a death-to-survival ratio of 1:4, indicating an overall mortality rate of approximately 20% in the selected dataset.
Hospitalisation (hosp_yn) aligns strongly with mortality rates, showing its predictive potential.
Geographic and Political Influence:
Political affiliations (Democrat vs Republican) and geographic distribution (res_state) may subtly influence the mortality outcomes.

Recommendations
  - Feature Engineering: Additional variables and interaction terms could improve predictions.
  - Model Diversity: Include more models like XGBoost or Neural Networks for comparison.
  - Generalisation: Validate with larger, unseen datasets.

### **Author**
**Tom Gibson**
