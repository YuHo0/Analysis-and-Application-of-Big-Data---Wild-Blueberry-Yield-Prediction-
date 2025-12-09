# Wild Blueberry Yield Prediction Analysis 🫐

A data science project that analyzes environmental and pollination factors to predict wild blueberry yield. This project utilizes statistical correlation techniques (Dendrograms, Heatmaps) and benchmarks multiple Machine Learning regression models.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square)
![ML](https://img.shields.io/badge/Machine%20Learning-Regression-orange?style=flat-square)
![Status](https://img.shields.io/badge/R%C2%B2%20Score-0.99-success?style=flat-square)

## 📖 Executive Summary

The goal of this project is to build a robust model to predict blueberry yield (`yield`) based on features such as bee density, temperature, and rain. The study addresses the challenge of agricultural variability by leveraging **Regression Algorithms**.

## 🛠️ Methodology

### 1. Data Preprocessing & EDA
* **Source:** Wild Blueberry Pollination Simulation Data (Kaggle).
* **Correlation Analysis:** Utilized **Heatmaps** and **Dendrograms** (hierarchical clustering) to identify and remove highly correlated features (multicollinearity reduction).
* **Feature Scaling:** Applied **MinMax Scaling** to normalize features like `clonesize`, `honeybee`, and temperature ranges, ensuring optimal model convergence.

### 2. Modeling Strategy
We implemented and compared three regression algorithms to establish a performance benchmark:
* **Linear Regression (LR):** Establishing a baseline for linear relationships.
* **Random Forest Regressor (RF):** Utilizing ensemble learning to capture non-linear patterns.
* **Decision Tree Regressor (DT):** Providing an interpretable model structure.

## 📊 Model Performance

We achieved exceptional predictive accuracy across all models. The **Linear Regression** model performed surprisingly well (R² ≈ 0.992), suggesting a strong linear relationship in the preprocessed dataset.

| Model | R² Score (Test) | Performance Insight |
| :--- | :--- | :--- |
| **Linear Regression** | **0.99204** | Highest accuracy; highly effective after feature scaling. |
| **Random Forest** | **0.98743** | Excellent predictive power, robust to complex interactions. |
| **Decision Tree** | **0.97500** | Good baseline, slightly higher variance than RF. |

## 🖼️ Visual Evidence

### 1. Feature Correlation Analysis
The heatmap below visualizes the correlation matrix used to identify redundant features (e.g., Temperature Ranges).

<p align="center">
  <img src="Wild Blueberry Yield Prediction/assets/heatmap.jpg" width="800" alt="Correlation Heatmap">
</p>

### 2. Model Prediction Analysis (Actual vs Predicted)
The following scatter plots demonstrate the alignment between **Actual Yield (X-axis)** and **Predicted Yield (Y-axis)**. The black line represents the ideal prediction (Perfect Fit).

| Linear Regression (R² ≈ 0.99) | Random Forest (R² ≈ 0.99) |
| :---: | :---: |
| <img src="Wild Blueberry Yield Prediction/assets/linear_regression.jpg" width="400"> | <img src="Wild Blueberry Yield Prediction/assets/random_forest.jpg" width="400"> |

#### Decision Tree Regressor (R² ≈ 0.98)
<p align="center">
  <img src="Wild Blueberry Yield Prediction/assets/decision_tree.jpg" width="500" alt="Decision Tree Plot">
</p>

---

## 📂 Project Structure

```text
Wild-Blueberry-Yield-Prediction/
├── main.py                 # Core analysis code (EDA + Modeling)
├── requirements.txt        # Python dependencies
├── data/                   # Dataset folder
│   └── WildBlueberryPollinationSimulationData.csv
├── assets/                 # Results images (Regression plots, Heatmaps)
└── README.md               # Project Report
```
