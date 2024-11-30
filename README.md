# Predicting Housing Prices with Regression Models

## Overview

This project provides a hands-on tutorial for predicting housing prices using the **California Housing Dataset**. The main goal is to showcase the complete **machine learning pipeline** for a regression task. Key steps include data preprocessing, feature engineering, model training, evaluation, and optimization. The tutorial emphasizes how **feature engineering** can enhance model accuracy and interpretability.

---

## Purpose

- Learn to preprocess data for regression tasks.
- Explore the effect of feature engineering on model performance.
- Train and evaluate regression models, including:
  - **Linear Regression**
  - **Decision Tree Regressor**
  - **Gradient Boosting Regressor**
- Perform **hyperparameter tuning** to optimize model performance.
- Visualize results to gain insights into data and model predictions.

---

## Dataset

### **Source**
The dataset is the **California Housing Dataset**, included in Scikit-learn.

### **Features**
| Feature Name        | Description                                   | Type    |
|---------------------|-----------------------------------------------|---------|
| **MedInc**          | Median income in the district                | Numeric |
| **AveRooms**        | Average number of rooms per household         | Numeric |
| **Population**      | Total population in the district             | Numeric |
| **MedHouseVal**     | Median house value (target variable)          | Numeric |

---

## Methodology

### **1. Data Exploration**
- Load the dataset using `fetch_california_housing` from Scikit-learn.
- Understand feature distributions and data structure.
- Identify potential data quality issues.

### **2. Data Preprocessing**
- Check for missing values and handle them if necessary.
- Scale features using `StandardScaler` to normalize ranges.
- Split data into **training (80%)** and **testing (20%)** sets.

### **3. Feature Engineering**
- Analyze feature correlations with the target variable using a heatmap.
- Create additional features like:
  - `RoomsPerHousehold`: Average number of rooms per household.
  - `PopulationPerHousehold`: Population per household.
- Select features with strong predictive power.

### **4. Model Training and Evaluation**
- Train and evaluate the following models:
  1. **Linear Regression**: A simple, interpretable baseline model.
  2. **Decision Tree Regressor**: Captures non-linear relationships.
  3. **Gradient Boosting Regressor**: Combines weak learners for high accuracy.
- Metrics Used:
  - **Mean Squared Error (MSE)**
  - **R-Squared (R²)**

### **5. Hyperparameter Tuning**
- Use `GridSearchCV` to optimize parameters for the Gradient Boosting model:
  - `n_estimators`
  - `learning_rate`
  - `max_depth`
- Compare the optimized model to baseline models.

### **6. Visualizations**
- **Predicted vs Actual**: Scatter plot to evaluate prediction accuracy.
- **Residual Analysis**: Check for patterns or biases in residuals.

### **7. Feature Importance**
- Use Gradient Boosting to analyze feature importance.
- Highlight key predictors such as `MedInc` and `AveRooms` with bar plots.

---

## Results and Insights

### **Key Findings**
1. **Gradient Boosting Regressor** achieved the best performance:
   - Lowest **MSE**
   - Highest **R²**
2. **Feature Importance**:
   - `MedInc` and `AveRooms` had the most significant impact on predicting house prices.
3. **Residual Analysis**:
   - The model effectively captured key data patterns without major biases.

### **Applications**
- Predict housing prices for real estate valuation.
- Identify key factors driving property values.

---

## How to Run

### Step 1: Clone the Repository
Clone the repository to your local machine:
```bash
git clone <repository-url>
cd Regression-Task-Housing-Dataset

```

### Step 2: Install Dependencies
Install the required Python libraries using the `requirements.txt` file:
```bash
pip install -r requirements.txt
```

### Step 3: Open the Jupyter Notebook
Launch the Jupyter Notebook to explore the project:
```bash
jupyter notebook Regression_Tutorial-Housing.ipynb
```

### Step 4: Run the Notebook
- Open `Regression_Tutorial-Housing.ipynb`.
- Execute each cell sequentially to preprocess data, train models, and visualize results.

---

## Tools and Libraries

- **Programming Language**: Python
- **Libraries**:
  - `pandas`, `numpy`: For data manipulation.
  - `matplotlib`, `seaborn`: For data visualization.
  - `scikit-learn`: For model training, evaluation, and preprocessing.

---

## Repository Structure

```
project-directory/
│
├── Regression_Tutorial-Housing.ipynb   # Jupyter Notebook for the tutorial
├── requirements.txt                    # List of dependencies
├── LICENSE                             # License information
├── README.md                           # Documentation
└── Regression_House_Pricing_Report.docx # Report for additional details
```

---

## Future Work

1. **Advanced Models**:
   - Experiment with neural networks for non-linear relationships.
2. **Feature Engineering**:
   - Explore additional features based on domain knowledge.
3. **Cross-Dataset Validation**:
   - Test the model on different datasets for broader generalization.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

## Author

This project was designed to demonstrate a complete regression pipeline using the California Housing Dataset. It aims to help learners and practitioners build, train, and optimize regression models effectively.

---
