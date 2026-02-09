## Notebooks

This project is organized into two main Jupyter notebooks:

### 1) `notebooks/01_eda.ipynb` — Exploratory Data Analysis (EDA)
This notebook focuses on exploring the dataset and understanding the structure and distribution of the features.

Main steps include:
- Loading the cleaned dataset from `adult_clean.csv`
- Basic dataset inspection (shape, data types, missing values)
- Exploratory visualizations using Matplotlib and Seaborn
- Identifying patterns and relationships between features and the target variable (`income`)

---

### 2) `notebooks/02_modeling.ipynb` — Machine Learning Pipeline
This notebook contains the full ML workflow, including data extraction from PostgreSQL and model training.

Main steps include:
- Connecting to a local PostgreSQL database using SQLAlchemy
- Reading training and test data using SQL queries (`adult` and `adult_test` tables)
- Selecting relevant features for modeling
- Splitting the data into train/test sets (where applicable)
- Building a Scikit-learn pipeline using:
  - `ColumnTransformer`
  - `OneHotEncoder` for categorical features
  - `StandardScaler` for numerical features
- Training a baseline classification model (Logistic Regression)
- Evaluating performance using:
  - Confusion Matrix
  - Classification Report
