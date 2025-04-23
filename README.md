# Revenue Trend and Growth Analysis for SaaS Company

## Overview

This project analyzes customer churn behavior for a subscription-based streaming service. A predictive model was developed to identify high-risk users, helping in retention strategy and reducing churn rate.

## Project Structure

### 1. Data Import and Exploration
- The dataset was loaded using Pandas and initially examined for structure, types, and null values. Summary statistics were generated to understand customer behavior.
- Exploratory Data Analysis (EDA) was conducted using Seaborn and Matplotlib to reveal relationships between churn and categorical variables such as subscription plan, country, and device used.

### 2. Data Preprocessing
- Missing values were handled using appropriate imputation strategies. Categorical columns were encoded using Label Encoding and One-Hot Encoding where necessary.
- Feature scaling was applied using StandardScaler to normalize numeric features for better model convergence.
- The target variable was binary (Churn = 0 or 1), and class imbalance was addressed using SMOTE oversampling.

### 3. Feature Selection and Engineering
- Correlation heatmaps and feature importance from a Random Forest classifier were used to select relevant features.
- Features such as total watch time and subscription age were engineered from existing columns to improve predictive power.

### 4. Model Building and Evaluation
- Multiple models were trained including Logistic Regression, Decision Trees, Random Forest, and XGBoost.
- Evaluation metrics like accuracy, precision, recall, F1-score, and confusion matrix were computed.
- XGBoost performed best with hyperparameter tuning and cross-validation applied for optimization.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

## Output

The final model achieved 76% overall accuracy. It performed especially well for retained customers with 91% precision, and identified churners with 65% recall, offering a useful foundation for retention strategies.

## How to Use

- ### Clone this repository:
  ```bash
  git clone https://github.com/ankheat/Healthcare-Predictive-modelling.git
  ```
- ### Navigate to the project folder:
  ```bash
  cd Healthcare-Predictive-modelling
  ```
- ### Install dependencies:
  ```bash
  pip install -r requirements.txt
  ```
- ### Run the Jupyter Notebook to execute the workflow.

## Future Improvements

- Incorporate behavioral metrics like content engagement or session duration.
- Enhance model precision using ensemble techniques and visualize churn risk using dashboards.
