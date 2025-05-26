# Predicting Rainfall in Australia Using Machine Learning Models

## Project Description

This project aims to predict whether it will rain the next day in various locations across Australia by applying and comparing multiple machine learning classification models. The focus is on utilizing historical weather data—such as temperature, humidity, pressure, and wind speed—to create reliable models that can forecast rainfall.

Accurate rainfall prediction has practical importance for agriculture, water resource management, and daily planning across Australia.

## Who Will Benefit and Why?

* **Farmers and Agricultural Planners:** Can make better-informed decisions about irrigation and crop management based on upcoming rainfall predictions.
* **Water Resource Managers:** Can optimize reservoir and water distribution systems to prepare for potential rainfall or drought.
* **Government Agencies:** Improved weather forecasting aids in disaster preparedness and public safety alerts.
* **Businesses and the Public:** Daily activities and operations can be better planned around expected weather conditions.

The use of machine learning models improves prediction accuracy compared to traditional methods, providing timely and actionable insights.

## Dataset

The dataset originates from the **Australian Rainfall Prediction** competition on Kaggle and contains daily weather observations from the **Australian Government’s Bureau of Meteorology**. It includes features such as temperature, humidity, wind speed, pressure, and categorical indicators like 'RainToday'. The target variable is 'RainTomorrow', indicating if it rained the following day.

Data used here was accessed via [Rattle's repository](https://bitbucket.org/kayontoga/rattle/src/master/data/weatherAUS.RData).

## Approach

Four machine learning classification models were implemented and evaluated for their rainfall prediction performance:

1. **K-Nearest Neighbors (KNN):** Classifies based on the closest data points in feature space.
2. **Decision Tree Classifier:** Builds a tree structure to split data by feature thresholds for classification.
3. **Logistic Regression:** Predicts probability of rainfall using a linear relationship between features and outcome.
4. **Support Vector Machine (SVM):** Finds the optimal boundary to separate rain/no-rain classes in the data.

Models were assessed with multiple metrics:

* Accuracy Score
* Jaccard Index
* F1 Score
* Log Loss (for Logistic Regression only)

This multi-metric evaluation ensured balanced consideration of precision, recall, and overall correctness.

## Key Findings

**Which model predicts rainfall most accurately?**

* Logistic Regression achieved the highest accuracy score of **83.8%**, outperforming KNN and Decision Tree models which had accuracies around **75.4%**.
* Logistic Regression also had the best Jaccard Index (**0.51**) and F1 Score (**0.68**), indicating a good balance between false positives and false negatives.

**How did other models perform?**

* KNN and Decision Tree showed moderate accuracy (\~75%), with similar Jaccard and F1 scores (\~0.40 and 0.57 respectively).
* SVM performed poorly with zero Jaccard and F1 scores, indicating it failed to classify rainfall effectively in this dataset.

**What about additional metrics?**

* Logistic Regression’s Log Loss was **0.38**, reflecting confident probability predictions.
* Linear Regression was also tested but is not appropriate for classification and had lower performance on regression metrics.

These results suggest that Logistic Regression is the most reliable model for this problem, given the available data.

## Conclusion

This project demonstrates that logistic regression is the most effective machine learning model for predicting rainfall in Australia among the tested classifiers. Its high accuracy and balanced performance metrics make it a suitable tool for practical rainfall forecasting applications. Other classifiers like KNN and Decision Trees showed reasonable but lower accuracy, while SVM did not perform well for this dataset.

## Recommendations

Future work could explore feature engineering to enhance model inputs and test ensemble methods to potentially improve prediction accuracy further. Additionally, incorporating more granular temporal or spatial data may lead to better localized forecasts. Regular retraining with updated data would keep the models current with changing weather patterns.

---

## Acknowledgments

This project was completed as part of the **Machine Learning with Python** course within the **Data Science Professional Certificate** by IBM.

---

## About the Authors

* **Joseph Santarcangelo** – PhD in Electrical Engineering specializing in machine learning applications in signal processing and computer vision; IBM Researcher.
* **Svitlana Kramar** – Contributor to the course materials and project resources.

**Project completed by:** Qazi Fabia Hoq
