# ML-Covid-Death-Predictor

## Overview

This project analyses and predicts patient outcomes using a dataset of medical and demographic features. he dataset originates from CDC’s Covid-19 database and was processed to predict the target variable death_yn (Yes/No). The notebook demonstrates a complete data science workflow, from preprocessing and exploratory data analysis to implementing and evaluating machine learning models.

## Features

- **Data Preprocessing**:
  - Handling categorical and numerical variables.
  - Converting object types to categorical.
  - Generating frequency tables.
  
- **Exploratory Data Analysis (EDA)**:
  - Visualising the proportion of outcomes across features.
  - Descriptive statistics for datasets.

- **Machine Learning Models**:
  - Linear Regression
  - Logistic Regression
  - Random Forest Classifier

- **Model Evaluation**:
  - Accuracy Score
  - Precision Score
  - Confusion Matrix
  - Cross-Validation

## Files

- `new_features_df1.csv`: The input dataset containing patient records.
- `ML_Notebook.ipynb`: Jupyter Notebook containing the entire analysis and code implementation.

### **Step 1: Install Prerequisites**  

To run the notebook, you need the following Python libraries installed:
- `pandas`
- `matplotlib`
- `sklearn`
- `numpy`
- `scipy`

Install the dependencies using pip:

```bash
pip install pandas matplotlib scikit-learn numpy scipy

### **Step 2: Introduction to Dataset**  
The notebook begins with a description of the dataset, which comprises 50,000 randomly selected records with 19 initial features. After cleaning, 11 independent variables and the target variable remain.
Key features include demographic information (e.g., age_group, sex, race, ethnicity) and others like hosp_yn, county_frequency_size, and political affiliation (party).

### **Step 3: Data Preprocessing**
Data Cleaning: The case_month and Profile features were removed due to multicollinearity.
Encoding: Categorical variables were converted to appropriate data types for model compatibility using Python libraries such as Pandas and Scikit-learn.

### **Step 4: Exploratory Data Analysis (EDA)**
Frequency tables were generated for categorical features, showing distributions such as:
death_yn: 8,390 (Yes), 31,557 (No)
hosp_yn: 6,379 (Yes), 33,568 (No)
Party affiliations: 26,784 (Democrats), 13,163 (Republicans).
Visualisation tools like histograms or bar plots (likely created) were used to identify trends.

### **Step 5: Model Development**
Data was split into training and testing datasets. The split size was evident from a training set of 27,962 rows and a test set of 11,985 rows.
Algorithms employed include:
Logistic Regression
Random Forest
Stacking Classifier
Pipelines for data preprocessing, including scaling and encoding, were integrated.

### **Step 6: Model Evaluation**
Metrics such as accuracy, precision, recall, and F1 scores were calculated. These metrics help evaluate the models' performance on classifying mortality (death_yn).

Key Insights
Mortality Correlations: The data showed a death-to-survival ratio of 1:4, indicating an overall mortality rate of approximately 20% in the selected dataset.
Demographics:
Age groups 65+ years and 50 to 64 years appeared as significant factors, representing 11,647 and 6,657 cases respectively.
White race (34,049 entries) dominated the dataset, followed by Black (4,536) and Asian (911).
Females (21,144) slightly outnumbered males (18,803).
Hospitalisation and Mortality:
Hospitalisation (hosp_yn) aligns strongly with mortality rates, showing its predictive potential.
Geographic and Political Influence:
Political affiliations (Democrat vs Republican) and geographic distribution (res_state) may subtly influence the mortality outcomes.

Recommendations
Feature Engineering: Enhancements in feature selection, such as aggregating related variables or creating interaction terms, may improve model predictability.
Model Comparison: Future iterations should include comparisons of multiple models' performance to ensure robustness.
Real-World Testing: The model should be validated using additional datasets for generalisability.








