# Customer Promotion Response Prediction

**Data Analytics Competition FIND IT! 2024 — Team AI Geniuses**

An end-to-end data analytics and machine learning project developed for **Data Analytics Competition FIND IT! 2024**.

The project focuses on predicting **the promotion stage at which a customer is likely to receive a promotional program** based on demographic and purchasing behavior data. The solution covers data analysis, preprocessing, machine learning, model evaluation, and deployment.

---

## 📌 Project Overview

Effective customer targeting requires an understanding of customer characteristics and purchasing behavior.

In this project, customer demographic and transaction-related features are analyzed to develop a predictive model for identifying the promotion stage associated with a customer.

The project aims to:

* Analyze customer demographic and purchasing behavior.
* Develop a classification model to predict `jumlah_promosi`.
* Compare multiple machine learning approaches.
* Improve prediction performance using ensemble learning.
* Deploy the selected model as a web-based application.

---

## 📊 Dataset

The dataset contains customer demographic and purchasing behavior features.

### Dataset Files

| File                 | Description                                   |
| -------------------- | --------------------------------------------- |
| `train_features.csv` | Training dataset containing customer features |
| `train_labels.csv`   | Training target labels (`jumlah_promosi`)     |
| `test_features.csv`  | Test dataset containing customer features     |

The dataset contains **3,817 training observations and 3,818 test observations**. The target variable is `jumlah_promosi`, representing the promotion stage associated with a customer.

### Main Features

The available customer information includes:

* Birth year
* Education
* Marital status
* Income
* Number of children
* Recency / days since last purchase
* Spending on fruits
* Spending on meat
* Spending on fish
* Spending on cake
* Purchases made with discounts
* Web purchases
* Store purchases
* Complaints
* Membership date

These features are used to represent different aspects of customer demographics and purchasing behavior.

---

## 🔎 Methodology

The project follows an end-to-end data science workflow:

```text
Dataset
   ↓
Exploratory Data Analysis
   ↓
Data Preprocessing
   ├── Feature Selection
   ├── Feature Engineering
   ├── Outlier Handling
   ├── Missing Value Imputation
   └── Feature Scaling
   ↓
Train-Validation Split
   ↓
Machine Learning
   ↓
Model Evaluation
   ↓
Weighted Ensemble
   ↓
Deployment
```

### 1. Exploratory Data Analysis

The dataset was explored to understand customer characteristics and purchasing behavior before model development.

### 2. Data Preprocessing

The preprocessing stage includes:

* Feature selection
* Feature engineering
* Outlier handling
* Missing value imputation
* Feature scaling
* 80:20 train-validation split

The preprocessing pipeline also applies model-based techniques for missing value imputation.

### 3. Model Development

Several machine learning approaches were evaluated, including:

* K-Nearest Neighbors
* Random Forest
* XGBoost
* CatBoost
* Neural Network
* FastAI
* Weighted Ensemble

A stacking-based ensemble approach was used to combine predictions from different models.

---

## 📈 Model Performance

The primary evaluation metric used in the project is **F1 Macro**.

| Model                    |     F1 Macro |
| ------------------------ | -----------: |
| **Weighted Ensemble L3** | **0.818968** |
| XGBoost L2               |     0.818968 |
| FastAI L2                |     0.815941 |
| CatBoost L2              |     0.811777 |
| Random Forest L2         |     0.810208 |
| CatBoost L1              |     0.762020 |
| XGBoost L1               |     0.757990 |
| FastAI L1                |     0.697313 |
| Neural Network L1        |     0.693847 |
| KNN L1                   |     0.557770 |

The **Weighted Ensemble L3** achieved an F1 Macro score of **0.818968 (81.90%)** and was selected for deployment.

---

## 🚀 Deployment

The selected model was deployed as a web application using:

* **Flask**
* **Google Cloud Run**
* **Large Language Model (LLM)** for generating additional descriptions after prediction

The deployed application allows users to provide customer information and obtain predictions through a web interface.

### Live Demo

**[aigeniuses.jemmyfebryan.site](https://aigeniuses.jemmyfebryan.site)**

---

## 📁 Repository Structure

```text
DAC_FindIT2024/
│
├── AIGeniuses.ipynb
├── Laporan FindIT2024.pdf
├── test_features.csv
├── train_features.csv
├── train_labels.csv
└── README.md
```

### Files

| File                     | Description                                                                                     |
| ------------------------ | ----------------------------------------------------------------------------------------------- |
| `AIGeniuses.ipynb`       | Jupyter Notebook containing the data analysis, preprocessing, modeling, and evaluation workflow |
| `Laporan FindIT2024.pdf` | Detailed project report                                                                         |
| `train_features.csv`     | Training features                                                                               |
| `train_labels.csv`       | Training target labels                                                                          |
| `test_features.csv`      | Test features                                                                                   |
| `README.md`              | Project documentation                                                                           |

---

## 🛠️ Tools & Technologies

**Programming & Data Analysis**

* Python
* Pandas
* NumPy
* Jupyter Notebook

**Machine Learning**

* Scikit-learn
* XGBoost
* CatBoost
* Random Forest
* FastAI

**Deployment**

* Flask
* Google Cloud Run
* Large Language Model (LLM)

---

## 👥 Team

### AI Geniuses

* **Jemmy Febryan**
* **German Mindo Simarmata**
* **Meirida Karisma Putri**

**Data Analytics Competition FIND IT! 2024**

---

## 📄 Project Report

For a detailed explanation of the analysis, preprocessing, modeling process, and results, see:

**[`Laporan FindIT2024.pdf`](./Laporan%20FindIT2024.pdf)**

The complete implementation can be explored in:

**[`AIGeniuses.ipynb`](./AIGeniuses.ipynb)**

---

## 💡 Key Takeaways

This project demonstrates an end-to-end machine learning workflow for customer analytics, including:

* Translating a customer promotion problem into a predictive modeling task.
* Working with demographic and purchasing behavior data.
* Performing data preprocessing and feature engineering.
* Comparing multiple machine learning models.
* Applying ensemble learning to improve prediction performance.
* Evaluating classification performance using F1 Macro.
* Deploying the final model as a web application.

The final deployed solution achieved an **F1 Macro score of 81.90%** on the validation set.
