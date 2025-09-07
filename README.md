# 🏠 House Price Prediction

## 📌 Project Overview
This project focuses on predicting house prices using machine learning techniques.  
The main objective is to explore the dataset, perform feature engineering, apply different ML models, and evaluate their performance to determine the most accurate model for price prediction.

---

## 📂 Dataset
- **Rows**: 20640 samples  
- **Features**: 10 variables including numerical and categorical features such as: [ocean_proximity ,..etc]
- **Target**: `median_house_value`

---
## 🔧 Exploratory Data Analysis
  - Visualize the count plot , pie plot and box plot of categorical columns with the Target .
  - get the mean price of houses based on ocean proximity
  - visualize the histogram plot and box plot for each numerical column to detect skewnesss and outliers.
  - 
## 🔧 Data Preprocessing
Steps applied to clean and prepare the data:
1. **Handling Missing Values** – filled using median after trying KNN Imputer( which medin was better).
2. **Handling Outliers** - Using IQR method.
3. **Encoding Categorical Variables** – Trying OneHot Encoding with get_dummies from pandas , after that applied like label encoder which was better than in modelling.
4. **Feature Scaling** – used MinMaxScaler for Features & target to avoid large numbers in prices which distributed the model.
5. **Feature Engineering** – choose best features with Recursive Feature Elimination.
6. **Train/Test Split** – divided data into training (80%) and testing (20%).

---

## 🤖 Models Implemented
Several models were trained and compared:
- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **Support Vector Machine**
- **KNN**

---

## 📊 Model Evaluation
Evaluation metrics:
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score**

|Model	           | Train RMSE	  |Test RMSE	  | Train R² (%)	| Test R² (%)
----------------------------------------------------------------------------
|Random Forest     | 0.074572	    |0.104863   	| 90.553086	    | 80.999050
----------------------------------------------------------------------------
|SVR	             | 0.122045     | 0.128370	  | 74.696386	    | 71.525219
----------------------------------------------------------------------------
|Decision Tree     | 0.000000	    | 0.132299	  | 100.000000	  | 69.755287
----------------------------------------------------------------------------
|KNN Regressor     | 0.105725	    | 0.136397	  | 81.010950	    | 67.852984
----------------------------------------------------------------------------
|Linear Regression | 0.145309	    | 0.149164	  | 64.130274	    | 61.553312
-----------------------------------------------------------------------------  


---

## 📈 Results & Insights
- The **Random Forest** model achieved the best performance but with overfitting. 

---

## Optimization 
- use Grid Search For every single model to get best parameters .
- use VotingRegressor & StackingRegressor with best estimators to get best performance.
