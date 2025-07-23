# 🛒 Big Mart Sales Prediction using XGBoost Regressor

This project uses the Big Mart dataset to predict the sales of different products at various outlet stores using Machine Learning, specifically the XGBoost Regressor algorithm.

---

## 📌 Dataset Description

The dataset contains information about various products across different outlets. It has two CSV files:
- **Train Dataset:** Includes features and target variable (Item_Outlet_Sales)
- **Test Dataset:** Includes only features (used for prediction)

---

## 📊 Features

- `Item_Identifier`: Unique product ID  
- `Item_Weight`: Weight of the product  
- `Item_Fat_Content`: Low Fat / Regular etc.  
- `Item_Visibility`: % of total display area  
- `Item_Type`: Snacks, Dairy, Beverages, etc.  
- `Item_MRP`: Maximum Retail Price  
- `Outlet_Identifier`: Store ID  
- `Outlet_Establishment_Year`: When the outlet started  
- `Outlet_Size`: Small / Medium / High  
- `Outlet_Location_Type`: Tier 1/2/3  
- `Outlet_Type`: Supermarket, Grocery Store, etc.  
- `Item_Outlet_Sales`: 🔥 **Target Variable**

---

## 🧹 Data Preprocessing

Data cleaning and preprocessing was a key part of this project. Here's what was done:

### ✅ Handling Missing Values
- **Item_Weight**: Filled using **median** value (numerical column).
- **Outlet_Size**: Filled using **mode** (most common category) – since it's a **categorical feature**.

### 🔁 Encoding Categorical Columns
- **Label Encoding** for ordinal features like `Outlet_Size`, `Outlet_Location_Type`, etc.

### 🔄 Feature Engineering
- Created **pivot tables to analyze** `Item_Type` vs `Item_Outlet_Sales`.
- Checked for feature importance using XGBoost’s built-in `.feature_importances_`.

---

## ⚙️ Model Used: XGBoost Regressor

- XGBoost handles overfitting well and works great for tabular data.
- Model was trained with train-test split.
- **Evaluation Metrics:**
  - MAE (Mean Absolute Error)
  - RMSE (Root Mean Squared Error)

---

## 🧠 Model Training

```python
from xgboost import XGBRegressor
model = XGBRegressor()
model.fit(x_train, y_train)

