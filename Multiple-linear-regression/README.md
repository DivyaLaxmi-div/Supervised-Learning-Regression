# Multiple Linear Regression - Calorie Burn Prediction 🔥

This project demonstrates **Multiple Linear Regression** using real-world datasets involving **exercise statistics** and **calorie consumption**. The goal is to predict the number of calories burnt based on various physical activity metrics.

---

## 📂 Dataset Description

The project uses two datasets:

1. **calories.csv** – Contains user IDs and the corresponding calories burned.
2. **exercise.csv** – Contains user-specific exercise metrics like duration, heart rate, and more.

These datasets were **merged** using pandas' `concat()` method based on row alignment.

---

## 🧠 Features Used

After preprocessing (like label encoding for gender), the following features were used for training:

- `Gender` (encoded)
- `Age`
- `Height`
- `Weight`
- `Duration`
- `Heart_Rate`
- `Body_Temp`

The target variable is:

- `Calories` (to be predicted)

---

## 🛠️ Model Used

- **Model:** `LinearRegression()` from `sklearn.linear_model`
- **Problem Type:** Regression (Multiple Linear Regression)
- **Evaluation Metric:** Mean Absolute Error (MAE)

---

## ✅ Steps Performed

- Loaded and explored both datasets
- Merged them into a single dataframe
- Performed basic preprocessing (e.g., encoding gender)
- Split the dataset into training and testing sets
- Trained a Multiple Linear Regression model
- Made predictions and evaluated performance

---

## 📈 Output

The model was able to **predict calorie burn** based on multiple physical attributes and exercise parameters.

---

## 📌 Technologies Used

- Python
- pandas
- numpy
- seaborn
- scikit-learn

---

## 📎 Sample Prediction

```python
input = (1, 68, 190.0, 94.0, 29.0, 105.0, 40.8)
model.predict([input])

