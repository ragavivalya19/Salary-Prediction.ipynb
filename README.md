AI Jobs Salary Prediction (2025–2026)
Project Overview
This project analyzes the AI Jobs Market 2025–2026 dataset and builds machine learning models to predict the annual salary of AI-related jobs. The goal of the project is to demonstrate a complete machine learning workflow starting from data loading and exploration to training and evaluating predictive models. The project helps understand how different job-related factors such as experience, education, company size, and location influence salary in the AI job market.
Dataset
The dataset used in this project is ai_jobs_market_2025_2026.csv, which contains information about AI job postings including job title, job category, experience level, years of experience, education required, city, country, company size, salary range, salary tier, and annual salary. In this project, annual_salary_usd is used as the target variable that the machine learning models attempt to predict.
Libraries Used
Several Python libraries are used in this project for data processing, visualization, and machine learning. Pandas is used for data manipulation and analysis, Matplotlib and Seaborn are used for visualization, Scikit-learn is used for preprocessing, model building, and evaluation, and SciPy is used to perform statistical testing such as ANOVA.
Data Loading and Initial Exploration
The dataset is uploaded using Google Colab and loaded using the Pandas library. Initial exploration is performed by checking for duplicate rows, identifying missing values in each column, and examining the data types of all columns. These steps help ensure that the dataset is clean and ready for further analysis and modeling.
Data Type Conversion
Certain columns such as job_title and education_required are converted into categorical data types because they represent categories rather than numerical values. Proper data typing ensures that the data is handled correctly during analysis and preprocessing.
Exploratory Data Analysis (EDA)
Exploratory data analysis is performed to understand relationships between variables in the dataset. A correlation matrix is calculated for all numerical features to identify relationships between them. A heatmap visualization is generated using Seaborn to clearly display these correlations, helping identify which variables may influence the target variable.
Statistical Analysis (ANOVA Test)
To determine whether categorical variables significantly influence salary, an ANOVA (Analysis of Variance) test is performed for each categorical column. The salary values are grouped by category and the ANOVA test calculates an F-statistic and p-value. If the p-value is less than 0.05, the variable is considered to have a statistically significant relationship with annual_salary_usd.
Feature Selection
Based on the dataset structure, a set of important features is selected for model training. The numerical features include is_senior, salary_max_usd, salary_min_usd, and years_of_experience. The categorical features include job_title, job_category, experience_level, education_required, city, country, company_size, and salary_tier. These features form the input variables used to predict the salary.
Feature Engineering
Before training the models, the features are transformed into a suitable format. Numerical features are standardized using StandardScaler to ensure that all numerical variables are on a similar scale. Categorical variables are converted into numerical form using One-Hot Encoding with the Pandas get_dummies() function. This step is necessary because machine learning models require numerical input data.
Train-Test Split
The dataset is divided into training and testing sets using an 80%–20% split. The training dataset is used to train the machine learning models, while the testing dataset is used to evaluate how well the models perform on unseen data.
Machine Learning Models[Salary_Prediction.ipynb](https://github.com/user-attachments/files/25874142/Salary_Prediction.ipynb)
[Salary_Prediction.ipynb](https://github.com/user-attachments/files/25874115/Salary_Prediction.ipynb)

Three machine learning regression models are used in this project. Linear Regression is used as a baseline model to capture linear relationships between features and salary. Random Forest Regressor is an ensemble learning model that builds multiple decision trees and combines their predictions to improve accuracy. Gradient Boosting Regressor is another ensemble technique that builds models sequentially and improves prediction performance by reducing errors from previous models.
Model Evaluation
The performance of the models is evaluated using three metrics. Mean Squared Error (MSE) measures the average squared difference between predicted and actual salary values. Mean Absolute Error (MAE) measures the average absolute difference between predictions and actual values. R² Score indicates how well the model explains the variance in the target variable. Higher R² scores and lower error values indicate better model performance.
Conclusion
This project demonstrates a complete machine learning pipeline including data preprocessing, exploratory data analysis, statistical testing, feature engineering, model training, and evaluation. The results help identify how different factors influence salary in the AI job market and show how machine learning models can be used to predict salary values based on job-related attributes.
