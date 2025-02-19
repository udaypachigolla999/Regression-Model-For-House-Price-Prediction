# Regression Model For House Price Prediction

## Project Overview
This project applies **Multiple Linear Regression (MLR)** to analyze the housing dataset (`Housing.csv`) and predict house prices based on various features. Additionally, **Recursive Feature Elimination (RFE)** was used in `MLR Housing Data RFE` to refine feature selection and improve model performance.

## Dataset: `Housing.csv`
### Features:
- `area` - Size of the house (in square feet)
- `bedrooms` - Number of bedrooms
- `bathrooms` - Number of bathrooms
- `stories` - Number of stories
- `mainroad` - Whether the house is on the main road (1: Yes, 0: No)
- `guestroom` - Availability of a guest room (1: Yes, 0: No)
- `basement` - Whether the house has a basement (1: Yes, 0: No)
- `hotwaterheating` - Availability of hot water heating (1: Yes, 0: No)
- `airconditioning` - Whether the house has air conditioning (1: Yes, 0: No)
- `parking` - Number of parking spaces
- `prefarea` - Whether the house is in a preferred area (1: Yes, 0: No)
- `furnishingstatus` - The furnishing status (`furnished`, `semi-furnished`, `unfurnished`)
- `price` - Target variable (House price)

## Methodology
1. **Data Preprocessing:**
   - Handled categorical variables by encoding `furnishingstatus` into dummy variables.
   - Normalized numerical features for better model performance.

2. **Feature Selection:**
   - Used **Recursive Feature Elimination (RFE)** in `MLR Housing Data RFE` to rank features based on importance.
   - Identified and removed highly correlated and insignificant variables using **Variance Inflation Factor (VIF) and p-values**.

3. **Model Building:**
   - Implemented **Ordinary Least Squares (OLS) Regression**.
   - Iteratively removed variables (`semi-furnished`, `bedrooms`, etc.) to refine the model.
   - Evaluated performance using Adjusted R² and p-values.

4. **Model Evaluation:**
   - Plotted residual analysis to check the normality of error terms.
   - Predicted house prices on test data and compared against actual values.
   - Final model achieved **R² = 0.6713** on the test set.

## Key Findings
- Removing highly correlated and insignificant variables improved model performance.
- `area`, `bathrooms`, `stories`, `mainroad`, `airconditioning`, `parking`, and `prefarea` were the most significant predictors of house price.
- The final model provides **a good balance between complexity and interpretability**.

## Usage
To reproduce the results, follow these steps:
1. Load the dataset (`Housing.csv`).
2. Run feature selection using **RFE** (optional, using `MLR Housing Data RFE`).
3. Train the **Multiple Linear Regression model**.
4. Evaluate the model using residual analysis and R² score.
5. Use the trained model to predict house prices.

## Tools & Libraries Used
- **Python** (Pandas, NumPy, Statsmodels, Scikit-learn, Matplotlib, Seaborn)
- **Jupyter Notebook** for implementation and visualization
