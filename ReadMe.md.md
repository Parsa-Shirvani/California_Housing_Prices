#  California Housing Price Prediction

##  Project Overview
This project explores the California Housing dataset to analyze factors influencing house prices and build predictive regression models.

The goal is to compare a linear baseline model with a non-linear ensemble model to understand how different algorithms capture relationships within the data.

---

##  Dataset
The dataset used in this project is the **California Housing dataset** available in `scikit-learn`.

It contains demographic and geographic information about California districts, including:

- Median Income
- House Age
- Average Rooms
- Average Bedrooms
- Population
- Average Occupancy
- Latitude & Longitude
- Median House Value (Target)

---

##  Exploratory Data Analysis (EDA)

During EDA, we:

- Checked data structure and verified no missing values
- Analyzed feature distributions
- Identified a ceiling effect in the target variable
- Explored geographic price patterns using spatial visualization
- Computed correlation between features and target

### Key Insights:
- **Median Income** is the strongest linear predictor of house prices.
- Coastal areas tend to have higher house values.
- Geographic effects appear non-linear.

---

##  Modeling Approach

We split the dataset into:
- 70% Training set
- 30% Testing set

Two models were trained:

1. **Linear Regression** (Baseline)
2. **Random Forest Regressor**

Feature scaling was not applied because:
- Tree-based models are not sensitive to feature scale.
- Linear Regression performs adequately without scaling in this context.

---

##  Model Performance

| Model             | MAE   | MSE   | R² Score |
| ----------------- | ----- | ----- | -------- |
| Linear Regression | 0.545 | 1.056 | 0.22     |
| Random Forest     | 0.343 | 0.280 | 0.79     |

###  Conclusion:
Random Forest significantly outperformed Linear Regression, indicating that non-linear relationships play an important role in predicting housing prices.

---

##  Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

##  Future Improvements
- Hyperparameter tuning
- Cross-validation
- Feature engineering
- Residual analysis