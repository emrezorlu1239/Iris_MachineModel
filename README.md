# 🌸 Iris Classification: End-to-End Machine Learning Project

> An end-to-end machine learning project comparing 5 different classification algorithms on the Iris dataset with hyperparameter tuning and detailed performance analysis.

## 📌 Project Overview
This project aims to classify Iris flowers into three distinct species (*Iris-setosa, Iris-versicolor, Iris-virginica*) based on their sepal and petal measurements. The notebook demonstrates a complete data science workflow, from Exploratory Data Analysis (EDA) to rigorous model evaluation.



## 🛠️ Models & Techniques Used
Five different machine learning algorithms were trained and evaluated:
1. **Logistic Regression** 2. **Support Vector Classifier (SVC)** (Linear Kernel)
3. **Gaussian Naive Bayes**
4. **Decision Tree Classifier**
5. **Random Forest Classifier**

**Key Techniques:**
* **Hyperparameter Tuning:** `GridSearchCV` with 5-fold Cross-Validation to find the optimal parameters (`C`, `solver`, `max_depth`, `n_estimators`, etc.) for each model.
* **Evaluation Metrics:** Evaluated models not just on **Accuracy**, but heavily emphasized **Log Loss** to measure the confidence of the predictions.
* **Visualizations:** Confusion matrices (using Seaborn heatmaps) and Feature Importance bar charts.

## 📊 Performance Comparison

All models achieved perfect accuracy on the test set, but analyzing the **Log Loss** reveals which models were the most "confident" in their predictions:

| Model | Accuracy | Log Loss |
| :--- | :--- | :--- |
| Logistic Regression | 100% | 0.1112 |
| SVC (Linear) | 100% | 0.0897 |
| Random Forest | 100% | 0.0533 |
| Gaussian Naive Bayes | 100% | 0.0263 |
| **Decision Tree** | **100%** | **0.0000** |

## 💡 Key Insights
* **Petals over Sepals:** Feature Importance analysis extracted from the Random Forest model shows that **Petal Length** and **Petal Width** are the most critical features for determining the species. Sepal measurements have minimal impact on the model's decision.
* **The "Setosa" Separation:** EDA and the Decision Tree structure revealed that *Iris-setosa* is linearly separable from the other two classes. A simple rule (e.g., `PetalLength <= 2.45 cm`) is enough to identify a Setosa flower with 100% certainty.

## 💻 Libraries Used
* `pandas` & `numpy` - Data Manipulation
* `matplotlib` & `seaborn` - Data Visualization
* `scikit-learn` - Machine Learning Modeling & Evaluation
**Prepared by:** [Emre Zorlu](https://www.kaggle.com/emrezorlu1239)
