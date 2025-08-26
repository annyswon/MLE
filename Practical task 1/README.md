## MLE Core Machine Learning Techniques

## Wine Quality Regression Report Summary  

### Objective  
The goal of this task was to predict wine quality scores using physicochemical properties of wine samples. Linear Regression and related models were applied to study the relationship between features such as acidity, sugar, alcohol, and density, and to evaluate how well these features explain wine quality.  

---

### Methodology  

**Mathematical Formulation**  
- The model is expressed as:  
  \[
  y = \beta_0 + \beta_1 x + \varepsilon
  \]  
  where:  
  - \(y\): dependent variable (wine quality).  
  - \(\beta_0\): intercept, the baseline quality when all predictors are 0.  
  - \(\beta_1\): coefficient, the expected change in quality for a one-unit change in \(x\).  
  - \(\varepsilon\): error term capturing unexplained variation.  

- Assumptions: linearity, independence of errors, homoscedasticity (constant variance), no multicollinearity, and normally distributed errors.  
- Violations: if these assumptions are not met, predictions may be biased, significance tests may be invalid, and overall model reliability can decrease.  

---

**Data Preprocessing**  
- Imported red and white wine datasets.  
- Checked for missing values (none found in the original dataset).  
- Removed duplicate rows.  

**Descriptive Statistics**  
- Computed mean, median, and standard deviation for each feature.  
- Identified potential outliers in variables such as residual sugar and sulphates using box plots.  

**Feature Engineering**  
- Created new features such as alcohol-to-density ratio.  
- Compared model performance before and after adding engineered features.  

**Univariate Analysis**  
- Histograms showed skewed distributions for some features (e.g., residual sugar).  
- Box plots highlighted extreme values in variables like chlorides.  

**Bivariate Analysis**  
- Scatter plots revealed positive relationships between alcohol and wine quality.  
- Correlation heatmap confirmed alcohol had the strongest positive correlation with quality, while volatile acidity had a negative correlation.  

**Dimensionality Reduction**  
- PCA reduced the dataset to two principal components.  
- First two components explained a meaningful portion of variance and allowed visualization of data spread.  

**Data Normalization**  
- Standardization and Min-Max scaling were applied.  
- Models trained on normalized data showed more stable coefficients but only slight changes in predictive performance.  

**Model Training and Evaluation**  
- Models: Linear Regression, Ridge, and Lasso.  
- Evaluation metrics: MSE, MAE, RMSE, and R².  
- Ridge regression provided slightly better generalization, while Lasso reduced the number of active features.  
- Residual plots showed non-perfect linearity but no major systematic bias.  

**Hyperparameter Tuning**  
- GridSearchCV used to optimize alpha values in Ridge and Lasso.  
- Tuned models achieved lower error and more stable predictions compared to defaults.  

---

### Findings & Insights  
- **Alcohol content** was the most important positive predictor of wine quality.  
- **Volatile acidity** was negatively associated with quality.  
- Feature engineering (alcohol-to-density ratio) improved model performance slightly.  
- Ridge regression was effective in reducing overfitting, while Lasso highlighted the most influential features.  
