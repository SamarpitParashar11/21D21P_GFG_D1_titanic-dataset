# 21D21P_GFG_D1_titanic-dataset

colab link : https://colab.research.google.com/drive/1OvHypt-k9kWkVxIzgfbWDb4RT_TyQXup?usp=sharing
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OvHypt-k9kWkVxIzgfbWDb4RT_TyQXup?usp=sharing)





# 🚢 Titanic Survival Analysis – End-to-End Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project performs a **comprehensive, end-to-end Exploratory Data Analysis (EDA)** on the famous **Titanic dataset** to understand the key factors that influenced passenger survival during the disaster.

The notebook is designed as a **step-by-step guide**, combining **theoretical explanations**, **data cleaning**, **visual analysis**, and **feature engineering**, making it ideal for beginners starting their **Data Science / Machine Learning journey**.

---

## 🎯 Project Objective

* Understand the structure and quality of the Titanic dataset
* Identify important features affecting survival
* Perform data cleaning and missing value handling
* Visualize distributions and relationships using statistical plots
* Engineer meaningful features for future machine learning models
* Generate an automated **data profiling report**

---

## 📚 What is Exploratory Data Analysis (EDA)?

Exploratory Data Analysis (EDA) is the process of:

* Understanding the dataset before modeling
* Discovering patterns and relationships
* Identifying missing values and outliers
* Validating assumptions required for ML models

EDA focuses on **data understanding**, not prediction.

---

## 🧰 Libraries Used

* **Pandas** – Data manipulation and preprocessing
* **NumPy** – Numerical computations
* **Matplotlib** – Base visualization library
* **Seaborn** – Statistical data visualization
* **ydata-profiling** – Automated EDA and profiling report

---

## 🗂 Dataset Information

* **Source:** Titanic Dataset
* **Rows:** 891 passengers
* **Columns:** 12 original features
* **Target Variable:** `Survived`

  * `0` → Did not survive
  * `1` → Survived

---

## 🔍 Project Workflow

### 1️⃣ Data Loading & Inspection

* Loaded dataset from GitHub
* Used `.head()`, `.tail()`, `.shape()`, `.info()`, `.describe()`
* Identified missing values in:

  * `Age`
  * `Cabin`
  * `Embarked`

---

### 2️⃣ Data Cleaning & Missing Value Handling

* **Age:** Filled using median (robust to outliers)
* **Embarked:** Filled using mode
* **Cabin:** Dropped due to excessive missing values (~77%)
* Created new feature:

  * `Has_Cabin` → Indicates cabin availability

---

### 3️⃣ Univariate Analysis

**Categorical Features:**

* Survived
* Pclass
* Sex
* Embarked
* SibSp
* Parch

**Numerical Features:**

* Age
* Fare

📊 Used:

* Count plots
* Histograms
* KDE plots
* Box plots

---

### 4️⃣ Bivariate Analysis

Analyzed relationship between **Survival** and:

* Passenger Class
* Gender
* Port of Embarkation
* Cabin availability
* Age

📈 Observations confirmed:

* *Women and children first*
* Strong class-based survival inequality

---

### 5️⃣ Feature Engineering

Created new meaningful features:

* **FamilySize** = SibSp + Parch + 1
* **IsAlone** → Passenger traveling alone
* **Title** → Extracted from passenger names (Mr, Mrs, Miss, Master, Rare)

These features significantly improved interpretability.

---

### 6️⃣ Multivariate Analysis

* Survival rate by **Pclass & Sex**
* Violin plots for **Age vs Sex vs Survival**
* Correlation heatmap for numerical features

---

### 7️⃣ Outlier Analysis

* Identified extreme outliers in **Fare**
* Discussed transformation strategies (e.g., log transformation)

---

### 8️⃣ Automated Data Profiling

Generated a full **ydata-profiling HTML report** after data cleaning:

* Missing values
* Distributions
* Correlations
* Warnings

📄 Output file:

```text
titanic_df.html
```

---

## 🧠 Key Insights

### 🔑 Strongest Predictors of Survival

* **Sex & Title:** Females (`Mrs`, `Miss`) had the highest survival rates
* **Passenger Class:** 1st > 2nd > 3rd
* **Age:** Children survived more than adults
* **Cabin/Fare:** Proxy for wealth → higher survival

### 📌 Additional Findings

* Small families (2–4 members) survived more
* Solo travelers had lower survival rates
* Passengers from **Cherbourg (C)** had better survival outcomes

---

## 🚀 Next Steps

* Apply **machine learning models** (Logistic Regression, Random Forest, XGBoost)
* Encode categorical variables
* Handle outliers using transformations
* Perform model evaluation and tuning

---

## 📁 Repository Structure

```
├── 1_Data_Storytelling_Analysing_Survival_on_the_Titanic.ipynb
├── titanic_df.html
├── README.md
```

---

## 🙌 Acknowledgements

* Titanic Dataset (Kaggle / UCI)
* Pandas & Seaborn documentation
* ydata-profiling library

---

## 👤 Author

**Samarpit Parashar**
Aspiring Data Scientist | Machine Learning Enthusiast

