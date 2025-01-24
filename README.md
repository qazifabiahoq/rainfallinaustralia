# Predicting Rainfall in Australia using Machine Learning Models

## Overview

This project focuses on predicting rainfall in Australia using machine learning models. The goal is to compare the performance of various classification models and evaluate their ability to predict rainfall outcomes based on a given dataset. A dataset containing information about Australian weather conditions, including features like temperature, pressure, humidity, and more, is used to predict whether it will rain the next day.

## Dataset

The dataset used in this project is from the **Australian Rainfall Prediction** competition on Kaggle. It consists of historical weather data for various locations in Australia and is intended to predict whether it will rain on the next day. The features include daily weather parameters like temperature, humidity, wind speed, and other factors that might affect rainfall prediction.

The original source of the data is the **Australian Government's Bureau of Meteorology**, and the latest data can be gathered from [this link](http://www.bom.gov.au/climate/dwo/).

Additionally, the dataset contains extra columns like 'RainToday', and the target column is 'RainTomorrow'. The data used for this project was gathered from [Rattle](https://bitbucket.org/kayontoga/rattle/src/master/data/weatherAUS.RData).

## Models Used

The following machine learning models were applied:

1. **K-Nearest Neighbors (KNN)**: This model predicts the target class based on the majority class of the nearest neighbors in the feature space.
2. **Decision Tree Classifier**: A decision tree model splits the data into subsets based on feature values, creating a tree structure that helps predict the outcome.
3. **Logistic Regression**: A linear model used for binary classification, it predicts the probability of the target variable belonging to a certain class.
4. **Support Vector Machine (SVM)**: A powerful classifier that works by finding the hyperplane that best separates the classes in the feature space.

## Metrics Used

The performance of each model was evaluated using the following metrics:

- **Accuracy Score**: This measures the overall accuracy of the model by comparing the predicted values with the actual values.
- **Jaccard Index**: This measures the similarity between the predicted and actual values by dividing the intersection of predicted and true values by the union.
- **F1 Score**: A metric that combines precision and recall, providing a balance between the two.
- **Log Loss**: This metric measures the uncertainty of the model's predictions, primarily used for classification problems that predict probabilities (only used for Logistic Regression in this case).

## Results

The results of the models were as follows:

| Metric              | KNN        | Decision Tree | Logistic Regression | SVM        | Linear Regression |
|---------------------|------------|---------------|---------------------|------------|-------------------|
| **Accuracy Score**   | 0.754198   | 0.754198      | 0.838168            | 0.722137   | N/A               |
| **Jaccard Index**    | 0.399254   | 0.399254      | 0.511521            | 0.000000   | N/A               |
| **F1 Score**         | 0.570667   | 0.570667      | 0.676829            | 0.000000   | N/A               |
| **Log Loss**         | N/A        | N/A           | 0.381038            | N/A        | N/A               |
| **MAE**              | N/A        | N/A           | N/A                 | N/A        | 0.256319          |
| **MSE**              | N/A        | N/A           | N/A                 | N/A        | 0.115721          |
| **R2**               | N/A        | N/A           | N/A                 | N/A        | 0.427130          |

## Best Model

**Logistic Regression** performed the best based on the **Accuracy Score** (0.838168), which is the most commonly used metric for classification problems. The **Jaccard Index** and **F1 Score** for Logistic Regression are also relatively high, indicating that the model is not only accurate but also performs well in balancing false positives and false negatives. Although the **Log Loss** for Logistic Regression is relatively low (0.381038), it was only applicable for this model.

In comparison, **SVM** showed poor performance with a **Jaccard Index** and **F1 Score** of 0.000000, indicating that the model was unable to effectively predict the classes.

## Acknowledgment

This project is part of the **Machine Learning with Python** course, which is a part of the **Data Science Professional Certificate** by IBM. The implementation of this project was conducted as part of the learning journey in applying machine learning algorithms to real-world datasets.

---

## About the Authors:
- **Joseph Santarcangelo** has a PhD in Electrical Engineering, with research focused on using machine learning, signal processing, and computer vision to determine how videos impact human cognition. Joseph has been working for IBM since completing his PhD.
- **Other Contributors**: **Svitlana Kramar**

**Completed By**: Qazi Fabia Hoq  
**This is part of the course "Machine Learning With Python" for Data Science Certification By IBM**
