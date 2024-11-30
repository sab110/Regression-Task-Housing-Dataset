# Predicting Housing Prices with Regression Models

## Overview

This project demonstrates a step-by-step approach to predicting housing prices using the **California Housing Dataset**. It covers essential stages of a machine learning pipeline, including:

1. Data loading and exploration.
2. Preprocessing and feature engineering.
3. Model training and evaluation.
4. Hyperparameter tuning and analysis.
5. Insights from visualizations and feature importance.

The primary focus is on how feature engineering impacts model accuracy and interpretability.

---

## Dataset

The **California Housing Dataset** is a well-known dataset that contains information about housing prices in California districts, including features such as:

- **Median Income (`MedInc`)**
- **Average Number of Rooms (`AveRooms`)**
- **Population**
- **Target Variable (`MedHouseVal`)**: Median house value.

---

## Steps in the Pipeline

### **1. Load and Explore the Dataset**
- Load the dataset using `fetch_california_housing` from Scikit-learn.
- Inspect data structure, types, and summary statistics.
- Identify key characteristics of the dataset, such as feature ranges and potential issues like missing values.

---

### **2. Data Preprocessing**
- **Handling Missing Values**: Although this dataset is clean, check for missing data as part of the preprocessing routine.
- **Feature Scaling**: Standardize features using `StandardScaler` to improve model performance.
- **Data Splitting**: Split the dataset into training (80%) and testing (20%) sets to evaluate model performance.

---

### **3. Feature Engineering**
- Analyze correlations between features and the target variable using a heatmap.
- Create new features based on domain knowledge, e.g.,:
  - **RoomsPerHousehold**: Average number of rooms per household.
  - **PopulationPerHousehold**: Average population per household.
- Identify features with the strongest predictive power.

---

### **4. Model Training and Evaluation**
#### Models Implemented:
- **Linear Regression**: Simple and interpretable baseline model.
- **Decision Tree Regressor**: Captures non-linear relationships but may overfit.
- **Gradient Boosting Regressor**: Combines weak learners (decision trees) to capture complex patterns effectively.

#### Evaluation Metrics:
- **Mean Squared Error (MSE)**: Measures the average squared error between predicted and actual values.
- **R-Squared (R²)**: Indicates the proportion of variance in the target explained by the model.

---

### **5. Hyperparameter Tuning**
- Perform hyperparameter tuning for **Gradient Boosting Regressor** using `GridSearchCV`.
- Optimize parameters such as:
  - `n_estimators`: Number of trees.
  - `learning_rate`: Step size for weight updates.
  - `max_depth`: Maximum depth of trees.
- Achieve improved model accuracy with optimized parameters.

---

### **6. Visualizing Results**
- **Predicted vs Actual Values**: Scatter plot comparing predictions to actual values.
- **Residual Analysis**: Visualize residuals to check for biases or patterns in the model's predictions.

---

### **7. Feature Importance Analysis**
- Analyze the importance of each feature in the Gradient Boosting model.
- Use bar plots to highlight key predictors of housing prices, such as `MedInc` and `AveRooms`.

---

### **8. Additional Insights**
#### **Target Variable Distribution**:
- Visualize the distribution of `MedHouseVal` to assess range and skewness.

#### **Pairwise Relationships**:
- Use scatter plots to explore relationships between features (e.g., `MedInc`, `AveRooms`) and the target variable.

---

## Results and Insights
- **Gradient Boosting Regressor** outperformed Linear Regression and Decision Tree models, achieving the lowest MSE and highest R².
- **Feature Importance Analysis** revealed that features like `MedInc` and `AveRooms` have the greatest impact on housing prices.
- **Residual Analysis** confirmed that the model predictions are unbiased and effectively capture key patterns in the data.

---

## Conclusion

This project showcases a complete machine learning pipeline, emphasizing:
1. The importance of preprocessing and feature engineering.
2. The value of hyperparameter tuning for model optimization.
3. Using visualizations to interpret results and identify potential improvements.

Future work could involve:
- Exploring advanced models like neural networks.
- Applying additional feature engineering techniques.
- Testing on other datasets for broader generalization.

---

## How to Run

1. Clone the repository and install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```
2. Run the code in a Jupyter Notebook or Python environment to replicate the results and visualizations.

---

## Dependencies

- Python (>=3.7)
- Libraries: `scikit-learn`, `numpy`, `pandas`, `matplotlib`, `seaborn`

---

## Author

This tutorial was crafted as an educational project to demonstrate the power of regression models in predicting housing prices.