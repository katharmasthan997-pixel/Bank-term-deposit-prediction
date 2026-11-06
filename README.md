# Bank Term Deposit Prediction Using Machine Learning

## Project Overview

This project uses machine learning to predict whether a bank customer is likely to subscribe to a term deposit through a telephone marketing campaign.

By analysing customer demographics, financial information, and previous campaign details, the system aims to help banks identify potential customers and make their marketing activities more effective.

## Problem Statement

Banks often contact a large number of customers to promote term deposits. However, many customers may not be interested in the offer. This can lead to unnecessary calls, increased marketing expenses, and wasted employee effort.

This project addresses the problem by developing a classification model that predicts customer subscription behaviour using historical banking data.

## Objectives

- Analyse customer information and previous marketing campaign results.
- Perform exploratory data analysis to understand the dataset.
- Clean and prepare the data for machine learning.
- Handle class imbalance using SMOTE.
- Train and compare multiple classification algorithms.
- Identify a suitable model for predicting term deposit subscriptions.

## Dataset Information

- **Dataset:** Bank Marketing Dataset
- **Source:** UCI Machine Learning Repository
- **Records:** 4,521
- **Columns:** 17 (16 input features and 1 target variable)
- **Target Variable:** `y` (renamed to `deposit`)
- **Problem Type:** Supervised Learning - Binary Classification

The target variable contains two possible outcomes:
- `yes`: Customer subscribed to a term deposit.
- `no`: Customer did not subscribe to a term deposit.

**Dataset link:** https://archive.ics.uci.edu/dataset/222/bank+marketing

## Technologies and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- Jupyter Notebook

## Project Workflow

1. **Data Loading:** Import the banking dataset and required Python libraries.
2. **Exploratory Data Analysis:** Examine the dataset using statistical summaries and visualizations.
3. **Data Preprocessing:** Handle missing values, duplicate records, and outliers.
4. **Encoding and Scaling:** Convert categorical variables into numerical format and scale numerical features.
5. **Feature Selection:** Apply SelectKBest and correlation analysis to identify useful features.
6. **Train-Test Split:** Divide the dataset into training and testing sets using stratified sampling.
7. **Class Imbalance Handling:** Apply SMOTE to balance the training data.
8. **Model Building:** Train different machine learning classification algorithms.
9. **Hyperparameter Tuning:** Use GridSearchCV with StratifiedKFold to search for suitable model parameters.
10. **Model Evaluation:** Compare model performance using accuracy, precision, recall, F1-score, and confusion matrices.

## Machine Learning Algorithms

The following classification algorithms were implemented:

- Decision Tree Classifier
- K-Nearest Neighbors (KNN)
- Random Forest Classifier
- Gaussian Naive Bayes
- Logistic Regression

## Model Performance

After model evaluation and hyperparameter tuning, the following accuracy scores were obtained:

| Algorithm | Accuracy |
|---|---:|
| Naive Bayes | 86.88% |
| Logistic Regression | 80.91% |
| KNN | 80.03% |
| Random Forest | 78.56% |
| Decision Tree | 76.57% |

### Best Performing Model

Gaussian Naive Bayes achieved the highest accuracy of **86.88%** among the evaluated models.

For the `yes` class, the model achieved:
- Precision: 0.44
- Recall: 0.54
- F1-score: 0.49

These results show that the model can identify some potential subscribers, although there is still scope to improve its ability to detect interested customers.

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/bank-term-deposit-prediction.git
```

### 2. Open the Project Folder

```bash
cd bank-term-deposit-prediction
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn openpyxl jupyter
```

### 4. Add the Dataset

Download the Bank Marketing dataset from the UCI repository and place the Excel file (`bank.xlsx`) in the project folder.

### 5. Run the Notebook

```bash
jupyter notebook
```

Open `Mini_Project.ipynb` and execute the cells in order.

**Note:** Update the dataset file path in the notebook according to where you save `bank.xlsx`.

## Project Outcome

This project demonstrates how machine learning can support banking marketing decisions by analysing customer data and predicting term deposit subscription behaviour. The results can help banks make more informed decisions when selecting customers for future campaigns.

## Future Improvements

- Improve the detection of customers who are likely to subscribe.
- Experiment with additional classification algorithms such as XGBoost.
- Apply a complete preprocessing and resampling pipeline to reduce data leakage risks.
- Evaluate models using business-focused metrics and threshold tuning.
- Develop a simple web application for interactive predictions.

## Reference

S. Moro, P. Rita, and P. Cortez (2014). *A data-driven approach to predict the success of bank telemarketing.* Decision Support Systems, Volume 62, Pages 22-31.

DOI: https://doi.org/10.1016/j.dss.2014.03.001

---

**Project Type:** Data Science Mini Project  
**Author:** Kathar Masthan A
