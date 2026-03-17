#  Machine Learning for Public Infrastructure Reliability: Predicting Water Well Status in Tanzania

##  Project Overview

Access to clean and reliable water remains a major challenge in Tanzania, where many water wells are either non-functional or in need of repair.

This project aims to build a **machine learning model** that predicts the condition of a water well based on its characteristics, such as location, construction details, and water quality.

The solution is designed to support **government agencies and NGOs** in identifying wells that require maintenance, enabling more efficient allocation of resources.

---

##  Objectives

* Predict the condition of a water well:

  * Functional
  * Functional but needs repair
  * Non-functional
* Identify key factors that influence well performance
* Provide actionable insights for infrastructure planning and maintenance

---

##  Dataset Description

The dataset contains information about **59,400 water wells** in Tanzania, including:

* Geographic data (latitude, longitude, region)
* Technical attributes (pump type, water source)
* Operational details (population served, payment type)
* Construction information (year built, installer, funder)

The target variable is **`status_group`**, representing the operational condition of each well.

---

##  Data Preprocessing

Several preprocessing steps were applied to prepare the data for modeling:

### Handling Missing Values

* Numerical features were imputed using the **median**
* Categorical features were imputed using the **most frequent value**

### Feature Engineering

* Created a new feature **`pump_age`** from construction year
* Handled invalid values (e.g., construction year = 0)

### Categorical Optimization

* High-cardinality features such as `installer` and `funder` were grouped into an **"Other"** category to reduce dimensionality

### Feature Selection

* Removed non-informative columns such as IDs and redundant variables
* Dropped duplicate categorical representations (e.g., grouped vs. class-based features)

---

##  Machine Learning Pipeline

A full **end-to-end pipeline** was built using Scikit-learn:

* Numerical preprocessing:

  * Missing value imputation
  * Standard scaling

* Categorical preprocessing:

  * Missing value imputation
  * One-hot encoding

* Model integration using a unified pipeline structure

This ensures reproducibility and prevents data leakage.

---

##  Models Used

The following models were trained and evaluated:

* **Random Forest Classifier**
* **Extra Trees Classifier**
* **Gradient Boosting Classifier**

---

##  Model Performance

| Model             | Accuracy |
| ----------------- | -------- |
| Random Forest     | 80.4%    |
| Extra Trees       | 79.4%    |
| Gradient Boosting | 75.9%    |

The **Random Forest model** achieved the best performance and was selected as the final model.

---

##  Key Insights

* **Geographic location** (latitude and longitude) is the strongest predictor of well functionality
* **Water quantity** (e.g., dry or insufficient) strongly indicates failure
* **Older wells** are more likely to be non-functional
* Wells serving larger populations may experience higher failure rates
* Infrastructure characteristics such as extraction type and waterpoint type influence performance

---

##  Limitations

* The model performs less effectively on the **"needs repair"** category due to class imbalance
* Geographic features dominate predictions, which may limit generalizability to new regions
* Further tuning and feature engineering could improve performance

---

##  Business Impact

This model can support:

* **Preventative maintenance planning**
* **Efficient allocation of repair resources**
* **Identification of high-risk regions**
* **Improved infrastructure decision-making**

Ultimately, the solution contributes to improving **access to clean and reliable water**.

---

##  Future Improvements

* Hyperparameter tuning for improved accuracy
* Advanced handling of class imbalance
* Incorporation of geospatial analysis
* Deployment as a decision-support tool

---

##  Conclusion

This project demonstrates the application of machine learning to a real-world infrastructure problem.

By leveraging data-driven insights, it is possible to identify failing water wells and support better planning and resource allocation, ultimately improving water access in Tanzania.

---
