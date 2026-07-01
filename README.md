# 🚚 Food Delivery Time Prediction using Machine Learning

## 📌 Project Overview

This project predicts **food delivery time (in minutes)** using machine learning based on factors such as distance, weather, traffic, vehicle type, preparation time, and courier experience.

The goal is to build a regression model that can estimate delivery time accurately and analyze which factors affect delivery performance.

---

## 📂 Dataset

The dataset contains **1000 delivery records** with the following features:

| Feature | Description |
|----------|-------------|
| Order_ID | Unique order identifier |
| Distance_km | Distance between restaurant and customer |
| Weather | Weather condition |
| Traffic_Level | Traffic intensity |
| Time_of_Day | Morning, Afternoon, Evening, Night |
| Vehicle_Type | Bike, Scooter, etc. |
| Preparation_Time_min | Food preparation time |
| Courier_Experience_yrs | Courier experience in years |
| Delivery_Time_min | **Target Variable** |

---

## 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## 📊 Exploratory Data Analysis (EDA)

Performed:

- Dataset inspection
- Missing value analysis
- Pairplot visualization
- Relationship analysis between features and target

---

## 🧹 Data Preprocessing

### Missing Value Handling

Categorical columns were filled using the **mode**:

- Weather
- Traffic_Level
- Time_of_Day

Numerical column:

- Courier_Experience_yrs → Median

---

### Feature Encoding

- Traffic_Level → Label Encoding (Ordinal)
- Weather → One-Hot Encoding
- Time_of_Day → One-Hot Encoding
- Vehicle_Type → One-Hot Encoding

---

### Feature Selection

Dropped:

- Order_ID (Unique identifier with no predictive value)

---

## 🤖 Model

**Algorithm Used**

- Linear Regression

---

## 📈 Model Performance

| Metric | Score |
|---------|-------|
| Mean Squared Error (MSE) | **101.36** |
| R² Score | **0.7739** |

### Interpretation

- The model explains approximately **77.4%** of the variance in delivery time.
- The average prediction error is approximately **10 minutes (RMSE ≈ 10.07 minutes)**.

---

## 📁 Project Structure

```
Food-Delivery-Time-Prediction/
│
├── Food_Delivery_Times.csv
├── Food_Delivery_Time_Prediction.ipynb
├── README.md
```

---

## 📌 Future Improvements

- Random Forest Regressor
- XGBoost Regressor
- Hyperparameter tuning
- Feature engineering
- Model deployment using Flask or Streamlit

---

## 📜 License

This project is intended for educational and learning purposes.
