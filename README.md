# Customer Promotion Response Prediction

**Data Analytics Competition FIND IT! 2024 — Team AI Geniuses**

An end-to-end data science project focused on predicting **the promotion stage at which a customer is likely to respond to a promotional program** based on demographic and purchasing behavior data.

The project covers the complete machine learning workflow, from **exploratory data analysis and data preprocessing to model development, evaluation, and deployment**.

---

## 📌 Project Overview

In the retail industry, understanding customer behavior is important for developing more targeted and effective promotional strategies.

This project uses customer demographic and purchasing behavior data to build a predictive model that can identify **when a customer is likely to respond to a promotional program**.

The final solution combines multiple machine learning models using a **Weighted Ensemble** approach and deploys the resulting model as a web-based application.

### Project Objectives

* Predict the promotion stage at which a customer is likely to respond.
* Identify customer patterns based on demographic and purchasing behavior.
* Improve the effectiveness of promotional targeting through data-driven analysis.
* Develop a machine learning solution that can be deployed and used through a web application.

---

## 📊 Dataset

The dataset contains customer demographic and purchasing behavior information.

### Main Features

| Feature                   | Description                                             |
| ------------------------- | ------------------------------------------------------- |
| `tahun_kelahiran`         | Customer's year of birth                                |
| `pendidikan`              | Customer's education level                              |
| `status_pernikahan`       | Customer's marital status                               |
| `pendapatan`              | Customer's income                                       |
| `jumlah_anak_balita`      | Number of children under five                           |
| `jumlah_anak_remaja`      | Number of teenage children                              |
| `terakhir_belanja`        | Number of days since the last purchase                  |
| `belanja_buah`            | Spending on fruit products                              |
| `belanja_daging`          | Spending on meat products                               |
| `belanja_ikan`            | Spending on fish products                               |
| `belanja_kue`             | Spending on cake products                               |
| `pembelian_diskon`        | Number of purchases made during discounts               |
| `pembelian_web`           | Number of online purchases                              |
| `pembelian_toko`          | Number of offline/store purchases                       |
| `keluhan`                 | Whether the customer has submitted a complaint          |
| `tanggal_menjadi_anggota` | Date when the customer became a member                  |
| `jumlah_promosi`          | Target: promotion stage at which the customer responded |

## The dataset consists of **3,817 training observations and 3,818 test observations**. The target variable `jumlah_promosi` represents the promotion stage at which a customer received the promotional program, with `0` indicating that the customer did not receive a promotion.

## 🔎 Methodology

The project follows an end-to-end machine learning workflow:

```text
Raw Dataset
     ↓
Exploratory Data Analysis
     ↓
Feature Selection
     ↓
Feature Engineering
     ↓
Outlier Handling
     ↓
Missing Value Imputation
     ↓
Feature Scaling
     ↓
Train-Validation Split
     ↓
Machine Learning Models
     ↓
Weighted Ensemble
     ↓
Model Evaluation
     ↓
Deployment
```

### 1. Exploratory Data Analysis

The dataset was explored to understand:

* Customer demographic characteristics
* Purchasing behavior
* Distribution of numerical features
* Categorical feature patterns
* Missing values
* Potential outliers
* Relationships between customer characteristics and promotional responses

### 2. Data Preprocessing

Several preprocessing techniques were applied:

* **Feature selection** to remove features with a high proportion of missing values or limited contribution.
* **Feature engineering**, including converting customer birth year into age and encoding categorical variables.
* **Outlier handling** for variables such as age and income.
* **Missing value imputation** using predictive models.
* **Feature scaling** using Standardization or Min-Max Scaling depending on the distribution of each feature.
* **Train-validation split** using an 80:20 ratio.

The preprocessing pipeline includes both traditional statistical techniques and machine-learning-based imputation.

---

## 🤖 Modeling

The project evaluates multiple machine learning approaches, including:

* K-Nearest Neighbors (KNN)
* Random Forest
* ExtraTrees
* XGBoost
* CatBoost
* Neural Network
* FastAI
* Weighted Ensemble

The main modeling strategy uses **stacking and weighted ensemble learning**. Models are trained in multiple stacks, where the predictions from earlier models are used as inputs for subsequent ensemble models.

The final model is a **Weighted Ensemble L3**.

---

## 📈 Model Evaluation

The primary evaluation metric is **F1 Macro**, which is used to evaluate the classification performance across the target classes.

### Validation Results

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

The **Weighted Ensemble L3 achieved an F1 Macro validation score of 0.818968 (81.90%)** and was selected as the main model for deployment.

---

## 🚀 Deployment

The selected model was deployed as a web application using:

* **Python**
* **Flask** as the web framework
* **Google Cloud Run** as the deployment platform
* **Large Language Model (LLM)** to provide additional descriptions after prediction

The deployment allows users to input customer information and obtain a model prediction through a web interface.

### 🌐 Live Demo

**[Open Deployment Website](https://aigeniuses.jemmyfebryan.site)**

---

## 📁 Repository Structure

```text
.
├── dataset/
│   └── [dataset files]
│
├── notebook/
│   └── [Jupyter Notebook]
│
├── report/
│   └── Laporan FindIT2024.pdf
│
└── README.md
```

### Repository Contents

| Folder / File | Description                                                              |
| ------------- | ------------------------------------------------------------------------ |
| `dataset/`    | Dataset used for the analysis and modeling                               |
| `notebook/`   | Complete data analysis, preprocessing, modeling, and evaluation workflow |
| `report/`     | Detailed project report                                                  |
| `README.md`   | Project overview and documentation                                       |

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
* ExtraTrees
* FastAI

**Deployment**

* Flask
* Google Cloud Run
* Large Language Model (LLM)

---

## 👥 Team

**Team AI Geniuses**

* Jemmy Febryan
* German Mindo Simarmata
* Meirida Karisma Putri

**Competition:** Data Analytics Competition FIND IT! 2024

---

## 📄 Project Report

For a more detailed explanation of the methodology, analysis, model development, and results, please refer to:

**`report/Laporan FindIT2024.pdf`**

---

## 💡 Key Takeaways

This project demonstrates an end-to-end approach to solving a customer analytics problem using machine learning:

* Translating a promotional business problem into a predictive modeling task.
* Working with demographic and customer behavioral data.
* Performing data cleaning, feature engineering, outlier handling, and missing value imputation.
* Comparing multiple machine learning algorithms.
* Combining models through a Weighted Ensemble approach.
* Evaluating models using F1 Macro.
* Deploying the final model into a web-based application.

The final solution achieved an **81.90% F1 Macro validation score** and was successfully integrated into a deployed application.
