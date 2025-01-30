# Credit-Risk-Classification

## Split the Data into Training and Testing Sets

### Instructions:
Open the starter code notebook and follow these steps to prepare the dataset for machine learning:

1. **Load the Dataset**  
   - Read the `lending_data.csv` file from the **Resources** folder into a Pandas DataFrame.

2. **Define Labels and Features**  
   - Create the **labels set (`y`)** from the `"loan_status"` column.
   - Create the **features set (`X`)** by selecting all remaining columns.

   **Note:**  
   - A value of `0` in the `"loan_status"` column indicates a **healthy loan**.  
   - A value of `1` means the loan has a **high risk of defaulting**.

3. **Split the Data**  
   - Use `train_test_split` to divide the data into **training (80%) and testing (20%) sets**.

These steps will prepare the dataset for training a machine learning model to predict **loan risk** effectively.

## Create a Logistic Regression Model with the Original Data

### Instructions:
Follow these steps to build and evaluate a **Logistic Regression** model for loan risk prediction:

1. **Train the Logistic Regression Model**  
   - Fit a logistic regression model using the training dataset (`X_train` and `y_train`).

2. **Make Predictions**  
   - Use the trained model to predict loan risk using the testing dataset (`X_test`).
   - Save the predictions for evaluation.

3. **Evaluate Model Performance**  
   - **Generate a Confusion Matrix** to visualize the accuracy of predictions.
   - **Print the Classification Report** to analyze **precision, recall, and F1-score** for both loan status categories.

4. **Analysis Question:**  
   - **How well does the logistic regression model predict both `0` (healthy loan) and `1` (high-risk loan) labels?**  
   - Examine the confusion matrix and classification report to determine the model’s strengths and weaknesses.

By completing these steps, we assess the **effectiveness of logistic regression** in predicting loan risk.

# Credit Risk Analysis Report

## Overview of the Analysis
The purpose of this analysis is to develop and evaluate a **machine learning model** for predicting **credit risk**. Using historical financial data, we trained a **Logistic Regression** model to classify loans as either **healthy (0)** or **high-risk (1)**. The goal is to help financial institutions make informed lending decisions by assessing the risk of default.

The dataset contains borrower financial details, including:
- Loan size
- Interest rate
- Borrower income
- Debt-to-income ratio
- Number of accounts
- Derogatory marks
- Total debt

We processed the data, split it into training and testing sets, and trained a **Logistic Regression** model to evaluate its performance.

---

## Results

### **Logistic Regression Model Performance**
- **Accuracy:** **99.27%**
- **Precision:**
  - **Class `0` (Healthy Loans):** **99.8%**
  - **Class `1` (High-Risk Loans):** **86.1%**
- **Recall:**
  - **Class `0` (Healthy Loans):** **99.5%**
  - **Class `1` (High-Risk Loans):** **93.9%**

**Confusion Matrix Insights:**
- **True Positives (476):** Correctly identified high-risk loans.
- **True Negatives (14,924):** Correctly identified healthy loans.
- **False Positives (77):** Misclassified healthy loans as high-risk.
- **False Negatives (31):** Misclassified high-risk loans as healthy.

---

## Summary

### **Model Performance Evaluation**
- The **Logistic Regression model** performed exceptionally well, achieving **over 99% accuracy**.
- The **high recall (93.9%) for high-risk loans** ensures that most risky cases are correctly identified.
- However, **31 high-risk loans were misclassified as healthy**, posing a potential risk for lenders.

### **Recommendation**
- If the priority is to **minimize false negatives** (avoiding risky loan approvals), alternative models like **Random Forest** or **Gradient Boosting** may improve results.
- If the focus is on **overall classification performance with minimal computational cost**, the **Logistic Regression model is a suitable choice**.
- Given the **high precision and recall**, this model is **recommended for financial institutions** seeking to balance **risk assessment and approval rates effectively**.

This analysis provides a **data-driven approach** to **credit risk prediction**, helping lenders make better financial decisions.

---

### **Next Steps**
- Further tuning of the model (e.g., adjusting hyperparameters or adding additional features).
- Exploring alternative classification models to **reduce false negatives**.
- Conducting additional validation using **real-world loan data**.

---
This report (inside of the Credit-Risk folder) is part of the **Credit Risk Analysis project**, providing insights into **loan approval decisions** using machine learning.


