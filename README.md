# 🧠 Predicting Loan Applicant Risk Profiles Using Machine Learning

### Commerce 3FN3 — Big Data in Finance | McMaster University  
**Author:** Adam Podolak  
**Tools Used:** Python, Pandas, NumPy, Scikit-Learn  

---

## 📘 Project Overview

This project explores how **machine learning can be applied to automate the risk assessment of loan applications**, helping financial institutions make faster, more consistent, and data-driven lending decisions.  

Each year, banks process thousands of loan applications manually — a process prone to **errors, inefficiencies, and compliance risks**. The goal of this project was to develop a **supervised learning model** that predicts the **risk profile** of loan applicants based on historical financial data.

---

## 🎯 Motivation

Traditional loan evaluation relies heavily on human judgment and manual review.  
Our motivation was to explore how **data science and automation** can:

- Reduce human bias and improve transparency in lending decisions.  
- Increase processing speed and scalability for banks during peak application periods.  
- Enable consistent risk profiling by learning from past loan outcomes.  

---

## 🧩 Dataset

- The dataset consisted of **15,000+ rows** and **19 financial parameters** per client, including income, payment history, loan amount, and previous defaults.  
- Data preprocessing included:
  - Removing high-cardinality categorical fields (e.g., *city*, *state*).  
  - Filling missing values using **median imputation** to preserve distribution consistency.  
  - Normalizing numerical fields to standardize model inputs.  

---

## ⚙️ Machine Learning Workflow

1. **Data Cleaning & Normalization** — Handle missing values and remove irrelevant columns.  
2. **Feature Selection** — Identify key predictors influencing loan repayment success.  
3. **Model Training** — Implemented six supervised learning algorithms:
   - Random Forest  
   - K-Nearest Neighbors (KNN)  
   - Gradient Boosting  
   - Naïve Bayes  
   - Logistic Regression  
   - Support Vector Classifier (SVC)  
4. **Evaluation** — Data split 70% training / 30% testing using Scikit-Learn’s `train_test_split()`.  
5. **Accuracy Comparison** — Visualized test vs. training performance to assess generalization.  

---
### ⚠️ Observations
- The **high training accuracy but low test accuracy** indicates **overfitting** — the models memorized training data patterns that didn’t generalize.  
- The **limited dataset size** and **low feature diversity** restricted model performance.  
- Expanding the dataset with **more samples, balanced class distributions**, and **richer features** (credit history length, employment status, debt ratios) would improve real-world accuracy.  

---

## 🧠 Skills & Concepts Learned

- **End-to-end machine learning pipeline** — from raw financial data to deployable model.  
- **Data wrangling and normalization** with `pandas` and `numpy`.  
- **Supervised learning techniques** using `scikit-learn`.  
- **Evaluation metrics** (accuracy, precision, recall) and cross-validation.  
- **Interpreting model limitations** due to data constraints.  
- **Business communication of ML insights** — translating accuracy scores into real financial implications.  

---

## 💼 Business Impact

- **Operational Efficiency:** Automated applicant scoring reduces manual review time.  
- **Scalability:** Systems can scale with loan volume by allocating additional compute resources.  
- **Risk Reduction:** Minimizes inconsistent human decisions and compliance errors.  
- **Customer Experience:** Faster loan decisions improve client satisfaction and retention.  

---

## 🧩 Future Improvements

- Gather larger and more balanced datasets across applicant demographics.  
- Implement **hyperparameter tuning** and **ensemble methods** to reduce bias/variance tradeoff.  
- Explore **deep learning approaches** (e.g., neural networks) once sufficient data is available.  
- Create a **front-end interface** for loan officers to interact with model predictions.  

---

## 🧾 Repository Structure

```plaintext
big_data_loan_risk_project/
|
│docs/
├── Big Data Report.pdf              # Full written report (methods, visuals, results, insights)
├── Big Data Report.pptx
├── Big Data Summary.pdf             # Presentation summary slides used for project defense
├── Big Data Summary.pptx
|
│src/
├── big_data_project.ipynb           # Initial data exploration and early ML setup
├── big_data_project_final.ipynb     # Final notebook with results and algorithm comparisons
├── financial_data.csv               # Cleaned and anonymized financial dataset
|
└── README.md                        # Project documentation (this file)
