
<h1 align="center">🧬 Medical Data Analytics: Calories Determination</h1>

<p align="center">
  <b>Author:</b> Enock Bereka • <b>Date:</b> February 15, 2025  <br>
  <b>Keywords:</b> Calories Prediction, Health Analytics, Linear Regression, R Programming
</p>

---

## 📌 Project Overview

This project aims to analyze the **factors influencing calorie expenditure** using a dataset of 15,000 individuals. The focus is on developing an accurate and interpretable regression model to predict calories burned based on vital signs and activity metrics.

---

## 🎯 Objectives

- 🔍 Explore and visualize key physiological variables.
- 📊 Understand the relationships between calorie expenditure and features like **age**, **heart rate**, **gender**, and more.
- 🧠 Build a robust **linear regression model** for prediction.
- 🧩 Investigate **interaction effects** and marginal influences.
- 🏆 Identify **top predictors** for accurate calorie estimation.

---

## 🧪 Dataset Summary

| Feature       | Description                         |
|---------------|-------------------------------------|
| `User_ID`     | Unique identifier                   |
| `Gender`      | Biological sex (male/female)        |
| `Age`         | Age in years                        |
| `Height`      | Height in cm                        |
| `Weight`      | Weight in kg                        |
| `Duration`    | Duration of activity in minutes     |
| `Heart_Rate`  | Heart rate during activity          |
| `Body_Temp`   | Body temperature in °C              |
| `Calories`    | Target variable: Calories burned    |

✅ Clean data with **no missing values or duplicates**.

---

## 📊 Exploratory Data Analysis

### Univariate Insights

- Distribution plots for age, height, weight, and more.
- Gender split shows balanced male and female data.
- Calories range from **1 to 314 kcal** with a mean of ~90 kcal.

### Bivariate Insights

- 🔥 **Strong positive correlation** between **Calories** and:
  - Duration
  - Heart Rate
- 🧊 **Negative correlation** between Calories and Body Temperature.

```r
ggcorrplot(cor(data[,-c(1,2)]))
```

---

## 📈 Modeling: Linear Regression

### 🔧 Model Features

```r
Calories ~ Gender + Age + Height + Weight + Duration + Heart_Rate + Body_Temp
```

### ✅ Assumption Checks

- No outliers (Cook's Distance)
- Residuals: Normally distributed
- No autocorrelation

### 📊 Performance

| Metric        | Value    |
|---------------|----------|
| Adjusted R²   | **0.967** |
| RMSE          | **11.311** |
| AIC           | 115,400+  |
| Residuals     | Normal    |

🎯 The model explains **96.7%** of variance in calories burned.

---

## 📌 Key Findings

| Predictor       | Impact on Calories        |
|-----------------|---------------------------|
| **Age**         | 🔼 Increases with age       |
| **Height**      | 🔽 Decreases with height    |
| **Weight**      | 🔼 Increases with weight    |
| **Duration**    | 🔼 Strongest influence      |
| **Heart Rate**  | 🔼 Strong positive impact   |
| **Body Temp**   | 🔽 Negative association     |
| **Gender (M)**  | Slightly fewer calories    |

📉 Gender difference was statistically significant (**p < 0.01**).

---

## 📌 Recommendations

- 🔁 **Deploy** the model in health tracking apps.
- 💓 Incorporate **heart rate and temperature sensors** in wearables.
- 🧠 Use **sex-specific models** for better personalization.
- 📲 Build a **Shiny dashboard** or interactive web app for predictions.
- 🚀 Test **advanced models** (e.g., Random Forests, XGBoost) for enhancement.

---

## 💼 Tools & Libraries

- **R Programming**
- `tidyverse`, `sjPlot`, `ggeffects`, `gtsummary`, `effectsize`, `vip`, `emmeans`, `car`, `performance`, `ggcorrplot`

---

## 📂 Project Structure

```
📦 Medical-Data-Analytics-Calories-Determination
 ┣ 📜 calories.csv
 ┣ 📊 EDA & Visualizations (R script)
 ┣ 📈 Linear Regression Model
 ┣ 📄 README.md
```

---

## 🙌 Acknowledgment

Thanks to the R community and open-source contributors whose tools made this analysis possible.

---

## 📬 Contact

**Enock Bereka**  

📍 Kakamega, Kenya  

🌐 [LinkedIn](https://www.linkedin.com/in/enock-bereka) • 📧 enock@example.com

> _"Transforming health through the power of data."_

---
