# 🏠 House Price Prediction

A machine learning project that predicts house prices using property characteristics such as area, bedrooms, bathrooms, stories, parking, and other categorical features.

## 📌 Project Objective

The objective of this project is to build a regression-based machine learning system that can estimate the price of a house from its available features.

The project follows this workflow:

```text
Raw House Data
      ↓
Data Cleaning
      ↓
Exploratory Data Analysis
      ↓
Feature Engineering
      ↓
Train / Test Split
      ↓
Regression Models
      ↓
Predicted House Prices
      ↓
RMSE / MAE / R²
      ↓
Model Optimization
```

## 📂 Dataset

The project uses `Housing.csv`.

- **Rows:** 545
- **Columns:** 13
- **Target variable:** `price`

The dataset contains numerical and categorical housing attributes.

Typical features include:

- `area`
- `bedrooms`
- `bathrooms`
- `stories`
- `mainroad`
- `guestroom`
- `basement`
- `hotwaterheating`
- `airconditioning`
- `parking`
- `prefarea`
- `furnishingstatus`

## 🔧 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## 🧹 1. Data Cleaning

The following preprocessing steps are performed:

- Check dataset shape and data types
- Check missing values
- Check duplicate records
- Remove exact duplicate rows
- Standardize categorical text values

## 📊 2. Exploratory Data Analysis

EDA is performed to understand the relationship between house characteristics and price.

Visualizations include:

- House price distribution
- Correlation heatmap
- Area vs. price scatter plot
- Price comparison by furnishing status

These visualizations help identify important patterns and relationships in the data.

## ⚙️ 3. Feature Engineering

The dataset contains both numerical and categorical features.

### Numerical Features

Numerical features are:

- Imputed using the median when necessary
- Standardized using `StandardScaler`

### Categorical Features

Categorical variables are:

- Imputed using the most frequent value
- Converted into numerical representations using `OneHotEncoder`

A Scikit-learn `ColumnTransformer` and `Pipeline` are used so preprocessing and model training remain consistent.

## ✂️ 4. Train/Test Split

The dataset is divided into:

- **80% Training Data**
- **20% Testing Data**

`random_state=42` is used to make the experiment reproducible.

## 🤖 5. Machine Learning Models

Multiple regression algorithms are trained and compared:

1. Linear Regression
2. Ridge Regression
3. Lasso Regression
4. Decision Tree Regressor
5. Random Forest Regressor
6. Gradient Boosting Regressor

## 📏 6. Model Evaluation

The models are evaluated using three metrics.

### RMSE — Root Mean Squared Error

RMSE measures the typical magnitude of prediction errors. A **lower RMSE indicates better performance**.

### MAE — Mean Absolute Error

MAE represents the average absolute difference between actual and predicted prices. Lower is better.

### R² Score

R² measures how much of the variation in house prices is explained by the model. Higher is generally better.

## 🎯 7. Model Optimization

Random Forest is further optimized using `GridSearchCV`.

The hyperparameters searched include:

- Number of estimators
- Maximum tree depth
- Minimum samples required for splitting
- Minimum samples required at a leaf

Five-fold cross-validation is used during hyperparameter tuning.

The optimized model is then evaluated on the test set.

## 📈 8. Prediction

The final model generates predicted house prices.

The notebook compares:

```text
Actual Price
     vs.
Predicted Price
```

An Actual vs. Predicted scatter plot is also created to visually evaluate model performance.

## 🗂️ Project Structure

```text
House-Price-Prediction/
│
├── Housing.csv
├── House_Price_Prediction_Project.ipynb
└── README.md
```

## ▶️ How to Run

### 1. Clone or download the project

Download the project files to your computer.

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open

```text
House_Price_Prediction_Project.ipynb
```

### 5. Run all cells

Make sure `Housing.csv` is in the same directory as the notebook.

## 💡 Key Machine Learning Concepts Demonstrated

This project demonstrates:

- Data preprocessing
- Exploratory Data Analysis
- Feature engineering
- One-hot encoding
- Feature scaling
- Train/test splitting
- Regression
- Model comparison
- RMSE, MAE and R² evaluation
- Cross-validation
- Hyperparameter tuning
- GridSearchCV
- Ensemble learning
- Prediction

## 🎤 Interview Explanation

> I developed a House Price Prediction project using supervised machine learning regression techniques. I first cleaned the housing dataset and performed exploratory data analysis to understand the relationship between different property features and house prices. I separated the target variable, price, from the input features and used a preprocessing pipeline to scale numerical variables and one-hot encode categorical variables. I trained multiple regression models including Linear Regression, Ridge, Lasso, Decision Tree, Random Forest and Gradient Boosting. I compared their performance using RMSE, MAE and R². Finally, I optimized the Random Forest model using GridSearchCV with five-fold cross-validation and selected the model based on the lowest RMSE.

## 🚀 Future Improvements

Possible improvements include:

- Adding more housing data
- Trying XGBoost or other advanced boosting algorithms
- Performing feature importance analysis
- Adding a Streamlit web application
- Saving the trained model using `joblib`
- Deploying the prediction application online
- Adding user input for real-time house price prediction

## 👨‍💻 Author

**Vansh Goel**

---

⭐ If you find this project useful, feel free to star the repository.
