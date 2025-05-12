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

### 5. Data Visualization
- Developed an interactive [Power BI dashboard](https://github.com/user-attachments/assets/2eda4446-cf2c-4294-ac6a-e71b0167e585) to highlight:
    - Key customer metrics including total revenue, churn rate, and lost revenue
    - Customer segmentation by subscription type, payment method, and genre preference (Active vs. Churned)
    - Churn behavior trends using visual analysis of support tickets, watchlist activity, and monthly revenue distribution

      ![image](https://github.com/user-attachments/assets/2eda4446-cf2c-4294-ac6a-e71b0167e585)




## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

## Output

- The XGBoost model with SMOTE and Grid Search achieved an overall accuracy of 76% at a threshold of 0.164. 
- While the model performs well in identifying the majority class (precision: 0.91), its performance on the minority class is moderate (recall: 0.65, f1-score: 0.49), highlighting a trade-off between precision and recall for rare events.

## How to Use

- ### Clone this repository:
  ```bash
  git clone [https://github.com/Bhuvi1901/ChurnAnalysis](https://github.com/Bhuvi1901/ChurnAnalysis)
  ```
- ### Navigate to the project folder:
  ```bash
  cd ChurnAnalysis
  ```
- ### Install dependencies:
  ```bash
  pip install -r requirements.txt
  ```
- ### Run the Jupyter Notebook to execute the workflow.

## Future Improvements

- Incorporate behavioral metrics like content engagement or session duration.
- Enhance model precision using ensemble techniques and visualize churn risk using dashboards.
