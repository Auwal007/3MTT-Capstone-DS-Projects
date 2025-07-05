# Insurance Premium Prediction - Capstone Project 1

## 🎯 Project Objective

This capstone project focuses on predicting insurance premium amounts using machine learning techniques. As part of the 3MTT (3 Million Technical Talent) program, this project demonstrates end-to-end machine learning workflow for regression problems in the insurance domain.

**Goal**: Build a predictive model to estimate insurance premiums based on customer demographics, policy details, and other relevant factors while gaining hands-on experience with data science methodologies.

## 📊 Dataset

The dataset contains insurance policy information with key features:
- **Demographics**: Age, Gender, Marital Status, Education Level, Number of Dependents
- **Financial**: Annual Income, Credit Score, Previous Claims
- **Health & Lifestyle**: Health Score, Smoking Status, Exercise Frequency
- **Policy Details**: Policy Type, Insurance Duration, Vehicle Age, Location, Property Type
- **Target Variable**: Premium Amount

**Dataset Size**: 278,860 records with 20 features

## 🛠️ Methodology

### Data Preprocessing
- Missing value handling using median/mode imputation
- Outlier treatment using IQR method
- Log transformation for skewed distributions
- Data type conversions and date processing

### Exploratory Data Analysis
- Distribution analysis for all features
- Correlation analysis with target variable
- Feature interaction exploration
- **Key Finding**: Numerical features showed weak linear correlation with premiums

### Feature Engineering
- **Policy Age**: Calculated from Policy Start Date
- **Premium to Income Ratio**: Most significant engineered feature
- **Income Brackets**: Quintile-based categories
- **Location-Property Interaction**: Combined categorical features

### Model Development
Trained and compared multiple regression algorithms:
- Linear Regression, Ridge, Lasso
- Decision Tree, Random Forest
- Gradient Boosting, XGBoost

**Best Model**: Random Forest Regressor (after hyperparameter tuning)

## 📈 Key Results

### Model Performance
- **Best Model**: Random Forest Regressor (after hyperparameter tuning)
- **Evaluation Metrics**: MAE, MSE, and R² Score used for model comparison
- **Cross-Validation**: 3-fold CV for robust performance estimation

### Important Findings
1. **Premium to Income Ratio**: Strongest predictor (engineered feature)
2. **Categorical Features**: Occupation, Policy Type, and Location are key drivers
3. **Feature Engineering**: Significantly improved model performance over raw features
4. **Insight**: Categorical segmentation more influential than individual numerical features

## 🚀 How to Reproduce Results

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

### Step-by-Step Instructions
1. **Setup Environment**
   ```bash
   # Navigate to the Capstone 1 directory
   cd "Capstone 1"
   ```

2. **Run the Analysis**
   ```bash
   jupyter notebook "capstone 1.ipynb"
   ```

3. **Execute all cells** in sequence from top to bottom
4. **Runtime**: Approximately 10-15 minutes for complete execution
5. **Note**: Ensure the dataset CSV file is in the same directory

## 📁 Project Structure
```
Capstone 1/
├── README.md
├── capstone 1.ipynb          # Main analysis notebook
├── Capstone_1_task.ipynb     # Task-specific notebook
└── Insurance Premium Prediction Dataset.csv
```

## 📚 Learning Outcomes

This capstone project demonstrates:
- **Data Preprocessing**: Handling missing values, outliers, and data transformations
- **Feature Engineering**: Creating meaningful features that improve model performance
- **Model Comparison**: Evaluating multiple algorithms and selecting the best performer
- **Cross-Validation**: Proper model validation techniques
- **Business Insights**: Translating model results into actionable findings

## 🔮 Future Enhancements
- Experiment with deep learning approaches
- Implement advanced feature selection techniques
- Add model interpretability using SHAP values
- Explore ensemble methods for better performance

---

**Note**: This is an educational capstone project for the 3MTT program, demonstrating machine learning concepts and techniques in the insurance domain for learning purposes.
