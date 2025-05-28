# Flight Price Prediction Project

This project aims to analyze flight booking data and build a predictive model to forecast flight ticket prices. The dataset was acquired from Kaggle and is believed to have originated from the "Ease My Trip" travel website.

##  Table of Contents
1. [Introduction](#introduction)
2. [Dataset Features](#dataset-features)
3. [Research Questions](#research-questions)
4. [Technologies Used](#technologies-used)
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
6. [Preprocessing & Feature Engineering](#preprocessing--feature-engineering)
7. [Modeling](#modeling)
8. [Results](#results)
9. [Conclusion](#conclusion)

---

##  Introduction

The primary objective of this study is to:
- Conduct a comprehensive analysis of flight booking data.
- Apply statistical hypothesis tests for meaningful insights.
- Build a machine learning model to accurately predict flight ticket prices.

---

## Dataset Features

| Feature             | Description                                                                 | Type            |
|---------------------|-----------------------------------------------------------------------------|-----------------|
| **Airline**         | Name of the airline                                                         | Categorical     |
| **Flight**          | Flight code                                                                 | Categorical     |
| **Source City**     | Departure city                                                              | Categorical     |
| **Departure Time**  | Binned time of departure                                                      | Categorical     |
| **Stops**           | Number of stops between source and destination                              | Categorical     |
| **Arrival Time**    | Binned time of arrival                                                        | Categorical     |
| **Destination City**| Arrival city                                                                | Categorical     |
| **Class**           | Seat class (Business/Economy)                                               | Categorical     |
| **Duration**        | Total travel time in hours                                                  | Continuous      |
| **Days Left**       | Days remaining until the trip date                                          | Derived         |
| **Price**           | Ticket price (Target Variable)                                              | Continuous      |

---

##  Research Questions

1. Does the price vary with Airlines?
2. How does the ticket price differ between Economy and Business class?
3. How is the price affected when tickets are bought just 1 or 2 days before departure?

---

##  Technologies Used

- **Python Libraries:**
  - `pandas`, `numpy` – For data manipulation
  - `seaborn`, `matplotlib`, `plotly` – For visualization
  - `scikit-learn` – For preprocessing, modeling, and evaluation
  - `TensorFlow/Keras` – For building Neural Networks

---

##  Exploratory Data Analysis (EDA)

### Visualizations
- Box plots were used to compare prices across airlines and classes.
- A pie chart was created to show the distribution of flight classes.
- Line and box plots illustrated how prices change as the departure date approaches.

---

##  Preprocessing & Feature Engineering

### Steps Taken:
- Dropped irrelevant column (`Unnamed: 0`)
- Label encoded all categorical variables
- Split the dataset into train, validation, and test sets
- Applied Min-Max scaling for numerical features

---

##  Modeling

Several regression models were implemented and evaluated:

| Model               | Description                                                   |
|---------------------|---------------------------------------------------------------|
| **Linear Regression** | Baseline model                                                |
| **Ridge Regression**  | Regularized linear model with hyperparameter tuning           |
| **Random Forest Regressor** | Ensemble method for capturing non-linear relationships |
| **Decision Tree Regressor** | Simple tree-based regressor                          |
| **Neural Network**      | Multi-layered deep learning model                         |

### Evaluation Metrics
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared (R² Score)

---

##  Results

- Linear Regression achieved an R² score of approximately X%.
- Ridge Regression improved performance slightly after hyperparameter tuning.
- Random Forest outperformed other models in terms of accuracy.
- Neural Network showed promising results but required more tuning for optimal performance.

---

##  Conclusion

This project successfully explored the relationship between various flight booking features and ticket prices. Through EDA and modeling, we found that factors like **airline**, **class**, and **days left before departure** significantly impact pricing. Among all models tested, **Random Forest Regressor** delivered the best predictive performance.

---

>  Future Work: Incorporate web scraping to update the dataset dynamically and deploy the model as a web application for real-time price prediction.

