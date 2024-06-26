## Customer Churn Analysis and Prediction

### Introduction
This project focuses on predicting customer churn using machine learning techniques. Customer churn refers to the phenomenon where customers cease their relationship with a company. Predicting churn can help businesses proactively take actions to retain customers

### Steps Taken
#### 1. Importing Libraries and Data
  - Libraries: Necessary Python libraries such as NumPy, Pandas, Matplotlib, Seaborn, Plotly, and warnings were imported.
  - Data: Loaded customer churn data from a CSV file using Pandas, and displayed the first few rows to understand its structure.
#### 2. Data Cleaning
  - Column Standardization: Converted all column names to lowercase to avoid typos during analysis.
  - Data Types Conversion: Converted the 'seniorcitizen' column to categorical ('Yes' or 'No') for better analysis and later encoding.
  - Handling Missing Values: Checked for missing values, found and dropped 11 rows with missing values, which was less than 1% of the dataset.
  - Handling Data Type Issues: Converted the 'totalcharges' column to numeric, stripping whitespace and handling errors coercively.
#### 3. Exploratory Data Analysis (EDA)
  - Categorical Variables Analysis: Plotted bar graphs for each categorical variable against churn to understand their impact.
  - Insights: Derived insights such as higher churn among customers without tech support, using fiber optic internet, etc.
  - Statistical Confirmation: Conducted Chi-squared tests to statistically confirm associations between categorical variables and churn.
#### 4. Feature Engineering
  - Preprocessing: Utilized Scikit-learn's ColumnTransformer for preprocessing numeric and categorical data separately.
  - Handling Imbalance: Addressed class imbalance using Synthetic Minority Over-sampling Technique (SMOTE) to balance the target variable distribution.
#### 5. Model Building and Evaluation
  - Baseline Models: Implemented several classification models (Logistic Regression, Random Forest, Gradient Boosting, etc.) to establish baseline performance metrics.
  - Evaluation Metrics: Evaluated models using accuracy, precision, recall, and F1-score via cross-validation.
  - Optimization Techniques: Explored techniques like PCA, Recursive Feature Elimination (RFE), and hyperparameter tuning (GridSearchCV) to enhance model performance.
  - Best Model Selection: Identified AdaBoostClassifier with SMOTE as the best-performing model based on F1-score.
#### 6. Hyperparameter Tuning
  - Optimization: Tuned hyperparameters of the AdaBoostClassifier using GridSearchCV to maximize F1-score.
  - ROC Curve Analysis: Plotted Receiver Operating Characteristic (ROC) curve to visualize model performance in terms of true positive rate vs. false positive rate.
#### 7. Prediction and Final Evaluation
  - Test Data Prediction: Applied the optimized model to predict churn on the final 100 rows of data.
  - Performance Metrics: Evaluated predictions using accuracy, precision, recall, and F1-score on the test dataset.
  - ROC Curve Validation: Confirmed model validity with a final ROC curve and area under the curve (AUC) calculation.

### Conclusion
This analysis and predictive modeling exercise illustrate a structured approach to understanding and predicting customer churn using machine learning techniques. The process involved thorough data cleaning, exploratory analysis, feature engineering, model selection, optimization, and validation. The insights gained and methodologies applied are essential for businesses looking to mitigate customer churn effectively.
