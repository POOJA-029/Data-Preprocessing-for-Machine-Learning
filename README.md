 Project Overview
This project performs comprehensive data preprocessing on the Boston Housing dataset to prepare it for machine learning modeling. The dataset contains various features related to housing in Boston, with the goal of predicting the median value of owner-occupied homes (MEDV).

📊 Dataset Information
Source: Boston Housing Dataset (commonly used in regression tasks)

Samples: 506

Features: 13 numerical features

Target Variable: MEDV (Median value of owner-occupied homes in $1000s)

Original Features:
CRIM: Per capita crime rate by town

ZN: Proportion of residential land zoned for lots over 25,000 sq.ft.

INDUS: Proportion of non-retail business acres per town

CHAS: Charles River dummy variable (1 if tract bounds river; 0 otherwise)

NOX: Nitric oxides concentration (parts per 10 million)

RM: Average number of rooms per dwelling

AGE: Proportion of owner-occupied units built prior to 1940

DIS: Weighted distances to five Boston employment centres

RAD: Index of accessibility to radial highways

TAX: Full-value property-tax rate per $10,000

PTRATIO: Pupil-teacher ratio by town

B: 1000(Bk - 0.63)² where Bk is the proportion of blacks by town

LSTAT: % lower status of the population

MEDV: Median value of owner-occupied homes in $1000s

🛠️ Preprocessing Steps
1. Data Loading & Initial Inspection
Loaded the dataset from house price.csv

Checked dataset shape, basic info, and descriptive statistics

Identified no missing values in the dataset

2. Data Type Identification
Identified categorical and numerical columns

Found 0 categorical columns and 13 numerical columns

Separated target variable (MEDV) from features

3. Preprocessing Pipeline Creation
Numerical Variables:

Missing value imputation using median strategy

Feature scaling using StandardScaler

Categorical Variables:

No categorical variables to process

4. Feature Engineering
Created a ColumnTransformer to handle all preprocessing steps

Applied preprocessing pipeline to all features

5. Train-Test Split
Split the dataset into training (80%) and testing (20%) sets

Used random_state=42 for reproducibility

6. Additional Analysis
Outlier Detection: Identified 40 potential outliers (7.9%) in the target variable

Correlation Analysis: Found strongest correlations with MEDV:

Positive: RM (0.70), ZN (0.36)

Negative: LSTAT (-0.74), PTRATIO (-0.51)

