# Bank_EDA_Project

# Retail Banking: Term Deposit Conversion Analytics

This repository contains an end-to-end data science project focused on predicting whether a retail banking customer will subscribe to a term deposit (also known as a Fixed Deposit).

## 📌 Project Overview & Business Value

In the competitive retail banking sector, telemarketing campaigns are a primary method for acquiring new term deposits. However, indiscriminately calling customers is inefficient, expensive, and can lead to customer fatigue. 

The goal of this project is to build a predictive model that identifies which customers are most likely to convert. By understanding the demographic, financial, and behavioral drivers of conversion, the bank can:
1. **Optimize Marketing Spend:** Focus telemarketing efforts only on high-probability targets.
2. **Improve Customer Experience:** Reduce the number of unwanted calls to customers unlikely to subscribe.
3. **Increase Revenue:** Improve the overall conversion rate and ROI of the campaign.

## 📊 Dataset Information

The data used in this project is based on a direct marketing campaign of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed.

**Target Variable:**
*   `deposit`: Has the client subscribed a term deposit? (binary: 'yes','no')

**Key Features Explored:**
*   **Demographics:** Age, Job, Marital Status, Education.
*   **Financial Health:** Balance, Default history, Housing loan, Personal loan.
*   **Campaign History:** Contact communication type, Last contact day/month, Number of contacts performed during this campaign.

*Note: The `duration` attribute (call duration) highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Therefore, to have a realistic predictive model that can be used *before* a call is made, this feature is excluded from the final training set.*

## 🛠️ Tech Stack & Methodology

*   **Language:** Python 3
*   **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
*   **Environment:** Jupyter Notebook

**Project Workflow:**
1.  **Exploratory Data Analysis (EDA):** Visualizing distributions, identifying patterns across occupations and financial statuses, and checking for missing values.
2.  **Data Preprocessing:** Handling categorical variables (One-Hot Encoding), scaling numerical features (StandardScaler), and addressing class imbalances.
3.  **Model Training:** Implementing and comparing multiple classification algorithms, including:
    *   Logistic Regression (Baseline)
    *   Random Forest Classifier
4.  **Model Evaluation:** Using Accuracy, Precision, Recall, F1-Score, and Confusion Matrices to determine the best-performing model for the business use case.
5.  **Feature Importance:** Analyzing which factors the model deemed most influential in predicting conversions.

## 🚀 Repository Contents

*   `Bank_EDA_Project_.ipynb`: The main Jupyter Notebook containing all the code for EDA, preprocessing, modeling, and evaluation.
*   `bank.csv`: The dataset used for this analysis.
*   `README.md`: Project documentation.

## 💡 How to Run the Project

1.  Clone this repository to your local machine.
2.  Ensure you have Python installed, along with the required libraries (`pip install pandas numpy scikit-learn matplotlib seaborn`).
3.  Open the Jupyter Notebook (`Axis_Bank_Credit_Conversion.ipynb`) and run the cells sequentially. Make sure `bank.csv` is in the same directory as the notebook.

## 📈 Key Findings & Insights

*(Note: These will be generated when you run the notebook, but typical findings include:)*
*   **Occupation Matters:** Management and retired individuals often show higher conversion rates.
*   **Financial Stability:** Customers with negative balances are highly unlikely to subscribe.
*   **Prior Success:** Customers who reacted positively to previous marketing campaigns are much more likely to subscribe again.
