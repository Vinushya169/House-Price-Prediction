
# 🏠 House Price Prediction

Predicting California house prices using Machine Learning — comparing Linear Regression, Decision Tree, and Random Forest to find the most accurate model.

[Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
[Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
[Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.3+-green.svg)
[License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 📌 Project Overview

House prices depend on multiple factors like income, location, number of rooms, and proximity to the ocean. This project builds a regression model to predict the `median_house_value` for California districts.

**Dataset:** California Housing Dataset  
**Rows:** 20,640 | **Columns:** 10  
**Target Variable:** `median_house_value`  
**Task Type:** Supervised Learning - Regression

---

## 📂 Dataset Description

| Column | Description |
| :--- | :--- |
| `longitude` | Longitude of the district |
| `latitude` | Latitude of the district |
| `housing_median_age` | Median age of houses in the district |
| `total_rooms` | Total number of rooms |
| `total_bedrooms` | Total number of bedrooms |
| `population` | Total population |
| `households` | Total households |
| `median_income` | Median income of households |
| `ocean_proximity` | Location w.r.t ocean (NEAR BAY, INLAND, etc.) |
| `median_house_value` | **Target** - Median house value |

---

## 🛠️ Technologies Used

- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn
- **Environment:** Jupyter Notebook
- **Version Control:** Git & GitHub

---

## 🔍 Exploratory Data Analysis (EDA)

- Checked shape, data types, missing values & duplicates
- Found **207 missing values** in `total_bedrooms` - filled with median
- Analyzed correlation of all features with `median_house_value`
- Visualized distributions using Histograms, Scatter Plots, Boxplots & Heatmap
- Key Insight: `median_income` has the strongest positive correlation with house price

## ⚙️ Feature Engineering

Created 3 new meaningful features to improve model performance:

```python
rooms_per_household = total_rooms / households
bedrooms_per_room = total_bedrooms / total_rooms
population_per_household = population / households
## 🧹 Data Preprocessing

- *Numeric Features:* Median Imputation + StandardScaler
- *Categorical Features:* One-Hot Encoding for `ocean_proximity`
- *Train-Test Split:* 80% Train / 20% Test (`random_state=42`)
- Used `ColumnTransformer` + `Pipeline` for clean and leak-free preprocessing

---

## 🤖 Models Trained

### 1. Linear Regression
Baseline model to understand linear relationships between features and price.

### 2. Decision Tree Regressor
Non-linear model with `max_depth=10` to capture complex patterns.

### 3. Random Forest Regressor
Ensemble model with `n_estimators=100` - combines multiple decision trees for higher accuracy.

---

## 📊 Results & Model Comparison
Model | MAE | RMSE | R² Score | Accuracy
Linear Regression | 50,000+ | 68,000+ | ~0.60 | ~60%
Decision Tree | 45,000+ | 65,000+ | ~0.65 | ~65%
**Random Forest** | **~32,000** | **~49,000** | **~0.80** | **~80%**
> *Note:* Values may vary slightly based on random state and preprocessing.

### 🏆 Best Model: Random Forest
Random Forest achieved the highest R² Score and lowest RMSE, making it the most accurate model for this dataset.

*Evaluation Metrics Used:*
- *MAE* - Mean Absolute Error
- *RMSE* - Root Mean Squared Error
- *R² Score* - How well the model explains variance

---

## 📁 Project Structure
House-Price-Prediction/
│
├── Housing.ipynb       # Main Jupyter Notebook with full code
├── housing.csv         # California Housing Dataset
└── README.md           # Project Documentation
---

## ▶️ How to Run This Project

*1. Clone the repository*
git clone https://github.com/Vinushya169/House-Price-Prediction.git
*2. Install required libraries*
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
*3. Run Jupyter Notebook*
jupyter notebook Housing.ipynb
Run all cells one by one to see outputs, graphs and model results.

---

## 🔮 Future Improvements

- [ ] Hyperparameter Tuning using GridSearchCV
- [ ] Try XGBoost / LightGBM for better accuracy
- [ ] Deploy model using Streamlit
- [ ] Add outlier handling for better performance

---

## 👩‍💻 Author

Vinushya M  
Aspiring Data Scientist | Machine Learning Enthusiast

🔗 GitHub: https://github.com/Vinushya169

---

## 📄 License

This project is licensed under the MIT License - feel free to use and modify.

Once you push it, open your GitHub link and it will look super professional. Send me the link after pushing, I will check it.
