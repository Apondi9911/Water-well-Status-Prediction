#  Machine Learning for Public Infrastructure Reliability: Predicting Water Well Status in Tanzania

##  ***Project Overview***

Access to clean and functional water sources is essential for communities.
This project aims to predict the condition of water wells (functional, needs repair, or non-functional) using available data.

### ***Objective***
The goal is to build machine learning models that can accurately classify the condition of a water well, helping organizations prioritize maintenance and resource allocation.

---

### ***Dataset Description and Understanding***

The dataset contains information about **59,400 water wells** in Tanzania, including:

* Geographic data (latitude, longitude, region)
* Technical attributes (pump type, water source)
* Operational details (population served, payment type)
* Construction information (year built, installer, funder)

The target variable is **`status_group`**, representing the operational condition of each well.

---
### ***Approach***
1. Data Cleaning & Preprocessing

This step involves handling missing values, correcting inconsistencies, and transforming raw data into a format suitable for modeling.

2. Feature Engineering

Informative features are created or existing ones are transformed to improve model performance ensuring the model captures patterns that may eventually influence the water well's operational status.

3. Model Building:
   - Logistic Regression (Baseline)
   - Random Forest (Advanced)
   - Ensemble Model (Voting Classifier)

4. Model Evaluation using Accuracy & Confusion Matrix
This provides a clear view of functional and non functional wells using the different model performances which are measured using accuracy, which reflects the proportion of correct predictions.

### ***Key Features***
- Reusable evaluation function
Using one single function that trains, predicts and evaluates any model using accuracy, classification report and confusion matrix ensuring testing of multiple models stay efficient and consistent.

- Pipeline-based preprocessing
This ensures that all transformations are applied consistently during training and testing, reducing errors and improving reproducibility.

- Ensemble learning
Combines predictions from multiple models (e.g., Logistic Regression and Random Forest) to make more accurate and stable predictions.


### ***Results***
- Random Forest outperformed baseline
- Ensemble model provided the best overall performance


### ***Recommendations***
- Use ensemble model for deployment
- Improve data quality for better predictions
- Prioritize repairs for wells predicted as non-functional as the older wells have declining water quantity.


### ***Limitations***
- Missing data in key fields
- Limited feature engineering

---

##  Conclusion

This project demonstrates the application of machine learning to a real-world infrastructure problem.
By leveraging data-driven insights, it is possible to identify failing water wells and support better planning and resource allocation, ultimately improving water access in Tanzania.

---

### ***Future Work***
- Hyperparameter tuning
- Geospatial modeling
- Handling class imbalance further