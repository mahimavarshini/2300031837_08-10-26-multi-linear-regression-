# 📈 Advertising Sales Prediction using Multiple Linear Regression

An end-to-end Machine Learning project predicting product sales based on advertising expenditures across Television (TV), Radio, and Newspaper channels using Multiple Linear Regression (MLR).

---

## 🎯 Objective
The primary objective of this project is to model the linear relationship between advertising expenditures across three marketing channels (TV, Radio, and Newspaper) and overall product sales volume. By quantifying channel coefficients and return on investment (ROI), the model helps business leadership optimize their marketing budget allocation and forecast future revenue with high predictive accuracy.

---

## 🛠️ Technologies Used
- **Programming Language:** Python 3.x
- **Data Manipulation & Analysis:** Pandas, NumPy
- **Machine Learning & Modeling:** Scikit-Learn (`LinearRegression`, `train_test_split`, `metrics`)
- **Evaluation Metrics:** R² Score, Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE)
- **Data Visualization:** Matplotlib, Seaborn
- **Environment:** Jupyter Notebook / VS Code

---

## 📊 Dataset Description
The dataset contains **200 market records** with 4 continuous variables:
* **Features ($X$):**
  * `TV`: Advertising spend in thousands of dollars ($k).
  * `Radio`: Advertising spend in thousands of dollars ($k).
  * `Newspaper`: Advertising spend in thousands of dollars ($k).
* **Target ($y$):**
  * `Sales`: Sales volume in thousands of units ($k units).

---

## ⚙️ Methodology & Project Structure
1. **Data Inspection & Quality Check:** Verified zero missing values and zero duplicate rows across 200 records.
2. **Exploratory Data Analysis (EDA):** Visualized individual spend vs. sales relationships with linear trendlines.
3. **Train-Test Split:** Partitioned data into 80% training (160 samples) and 20% testing (40 samples) with `random_state=42`.
4. **Model Training:** Fitted a `LinearRegression` model using scikit-learn.
5. **Model Evaluation:** Evaluated test performance using MAE, MSE, RMSE, and $R^2$ score.
6. **Scenario Forecasting:** Predicted sales for the planned marketing allocation (TV = $150k, Radio = $20k, Newspaper = $30k).
7. **Diagnostic Visualizations:** Model fit evaluation with Actual vs. Predicted scatter plot and sorted comparative bar chart.
8. **Business Insights & Recommendations:** Budget optimization and technical improvement strategies.

---

## 📈 Key Results & Metrics

| Metric / Parameter | Value |
| :--- | :--- |
| **Model Intercept ($\beta_0$)** | **4.7141** |
| **TV Coefficient ($\beta_1$)** | **0.0545** (+55 units per $1k spend) |
| **Radio Coefficient ($\beta_2$)** | **0.1009** (+101 units per $1k spend — **Highest ROI**) |
| **Newspaper Coefficient ($\beta_3$)** | **0.0043** (+4 units per $1k spend — **Negligible**) |
| **R-Squared ($R^2$) Score** | **0.9059 (90.59%)** |
| **Mean Absolute Error (MAE)** | **1.2748** thousand units (~1,275 units) |
| **Mean Squared Error (MSE)** | **2.9078** |
| **Root Mean Squared Error (RMSE)** | **1.7052** thousand units |
| **Planned Budget Forecast** | **15.0395** thousand units (~15,040 units) |

### Fitted Regression Equation:
$$\text{Sales} = 4.7141 + 0.0545 \times \text{TV} + 0.1009 \times \text{Radio} + 0.0043 \times \text{Newspaper}$$

---

## 📊 Visualizations Included
* **Graph 1 — Feature Spend vs. Sales (EDA):** 3-panel scatter plot with trendlines illustrating individual channel effects.
* **Graph 2 — Actual vs. Predicted Scatter Plot:** Demonstrates high model fit along the 45-degree reference line ($y = x$).
* **Graph 3 — Sorted Actual vs. Predicted Comparison:** Orderly bar chart comparing actual vs. predicted sales across all test samples.

---

## 💡 Business Recommendations
1. **Reallocate Budget:** Shift the planned **$30,000 Newspaper budget** into **Radio and TV**. Newspaper yields only ~4 units per $1k spend, whereas Radio generates ~101 units per $1k spend (over 23× more productive). Reinvesting this $30k into Radio yields an estimated **+3,000 additional units** without increasing total budget.
2. **Technical Improvements:**
   * Apply **K-Fold Cross-Validation** (5-fold / 10-fold) for enhanced validation stability.
   * Add cross-channel **Interaction Terms** $(\text{TV} \times \text{Radio})$ to capture multi-channel synergy effects.

---

## 🚀 How to Run Locally

### Prerequisites
Install the required Python packages:
```bash
pip install pandas numpy matplotlib scikit-learn
