# Gradient Boosting Regression on the Energy Efficiency Dataset

## Introduction
This project aims to predict the **Heating Load** of buildings using the **Energy Efficiency dataset** from the UCI Machine Learning Repository. We apply the **Gradient Boosting Regressor** — a powerful ensemble learning method — to model the relationship between various building design parameters and their energy efficiency.

The Gradient Boosting algorithm builds an ensemble of decision trees in a stage-wise manner, correcting errors at each step, which leads to high predictive accuracy on structured tabular data. The project follows a clear workflow, covering data preprocessing, model training, evaluation, and visual interpretation.

---

## Dataset Overview
The dataset includes **768 samples** and **10 features** representing building design parameters:

| Feature | Description |
|---------|-------------|
| x1 | Relative Compactness |
| x2 | Surface Area |
| x3 | Wall Area |
| x4 | Roof Area |
| x5 | Overall Height |
| x6 | Orientation |
| x7 | Glazing Area |
| x8 | Glazing Area Distribution |
| y1 | Heating Load (Target) |
| y2 | Cooling Load (Not used in this project) |

- **Train set size:** (537, 8)  
- **Test set size:** (231, 8)  

---

## Objective
The goal is to predict **Heating Load** (`y1`) using the eight design features (`x1`–`x8`) with high accuracy using Gradient Boosting.

---

## Model Evaluation  
The model is evaluated using two key metrics:  

| **Metric** | **Value** |  
|-----------|-----------|  
| **R² (Coefficient of Determination)** | ≈ 0.9981 |  
| **Mean Squared Error (MSE)** | ≈ 0.1922 |  

- The R² score of **0.9981** indicates that the model explains **99.81%** of the variance in Heating Load — a near-perfect fit.  

---

## Visualizations  
### 1. **Scatter Plot (Actual vs. Predicted)**  
- Confirms that predicted values closely align with actual values.  
- Data points lie close to the diagonal line.  

### 2. **Residual Histogram**  
- Centered around zero, indicating unbiased predictions.  
- Minimal spread confirms low prediction error.  

### 3. **Sorted Actual vs. Predicted Values**  
- Tight overlap of sorted actual and predicted values reflects a strong model fit.  

### 4. **Feature Importance Bar Chart**  
**Top 3 important features:**  
- **Roof Area**  
- **Relative Compactness**  
- **Surface Area**  

### 5. **Partial Dependence Plot (PDP)**  
- PDP for **Relative Compactness** shows that increased compactness lowers Heating Load.  

---

## Results and Insights  
✅ **High Predictive Power:**  
- **R² ≈ 0.9981** reflects near-perfect prediction capacity.  
- **MSE ≈ 0.1922** confirms low variance in residuals.  

✅ **Key Insights:**  
- **Roof Area** and **Compactness** are the most influential predictors.  
- Model performance suggests that building design factors have direct, predictable effects on Heating Load.  
- No significant bias or systematic under/over-estimation based on residual analysis.  

---

## Potential Improvements  
### 🔧 **Hyperparameter Tuning:**  
- Use **GridSearchCV** or **RandomizedSearchCV** to optimize `n_estimators`, `learning_rate`, and `max_depth`.  

### 🔁 **Cross-Validation:**  
- Implement **K-fold cross-validation** to test model robustness.  

### 🎯 **Feature Engineering:**  
- Introduce interaction terms or polynomial features for complex relationships.  

### 🛠️ **SHAP/ICE Analysis:**  
- Use **SHAP** (SHapley Additive exPlanations) and **ICE** (Individual Conditional Expectation) for more transparent feature attribution.  


## Installation
Clone the repository:
```bash
git clone https://github.com/DEEPIKAKASTURI/Machine-Learning-01.git
