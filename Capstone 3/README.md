# Employee Burnout Prediction - Capstone Project 3

## 🎯 Project Objective

This capstone project focuses on predicting employee burnout rates using machine learning techniques. As part of the 3MTT (3 Million Technical Talent) program, this project simulates a real-world scenario where we work as data scientists at NeuroWell Analytics to address the growing concern of employee burnout in organizations.

**Goal**: Build a predictive model to identify employees at risk of burnout and provide actionable insights for proactive intervention.

## 📋 Problem Statement

Employee burnout is a critical workplace issue affecting productivity, morale, and organizational health. This project aims to:
- Analyze employee data to identify burnout patterns
- Develop machine learning models to predict burnout rates
- Generate insights for HR teams to implement preventive measures

## 🛠️ Approach & Methodology

### Phase 1: Problem Understanding
- Researched employee burnout and its organizational impacts
- Analyzed the importance of data-driven burnout prevention

### Phase 2: Exploratory Data Analysis (EDA)
- Data inspection and quality assessment
- Statistical analysis of employee features
- Visualization of relationships between variables
- Missing value analysis and treatment strategy

### Phase 3: Data Preprocessing
- **Missing Data Handling**: Used KNN Imputation for numerical features
- **Feature Engineering**: Created tenure feature from joining dates
- **Categorical Encoding**: Applied one-hot encoding for categorical variables
- **Normalization**: Applied MinMax scaling to numerical features

### Phase 4: Model Development
- Implemented multiple algorithms:
  - Linear Regression
  - Decision Tree Regressor
  - Random Forest Regressor
  - Gradient Boosting Regressor
- **Best Model**: Gradient Boosting with hyperparameter tuning
- Performance optimization using GridSearchCV

## 📊 Dataset Information

| Column | Description |
|--------|-------------|
| Employee ID | Unique identifier for each employee |
| Date of Joining | Employee's start date |
| Gender | Employee gender |
| Company Type | Service-based or Product-based |
| WFH Setup Available | Work-from-home setup availability |
| Designation | Employee seniority level |
| Resource Allocation | Daily hours allocated |
| Mental Fatigue Score | Employee stress rating |
| **Burn Rate** | Target variable - burnout rate |

## 🚀 How to Reproduce Results

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Step-by-Step Instructions

1. **Clone/Download the project**
   ```bash
   # Navigate to the Capstone 3 directory
   cd "Capstone 3"
   ```

2. **Open the Jupyter Notebook**
   ```bash
   jupyter notebook capstone_3.ipynb
   ```

3. **Run the cells sequentially**:
   - **Data Loading**: Load train and test datasets from Google Drive
   - **EDA**: Execute exploratory analysis and visualizations
   - **Preprocessing**: Handle missing values and feature engineering
   - **Model Training**: Train multiple models and compare performance
   - **Hyperparameter Tuning**: Optimize the best-performing model

4. **Key Execution Notes**:
   - Ensure internet connection for Google Drive data loading
   - Missing values in 'Burn Rate' (~5%) are dropped
   - KNN Imputation is used for 'Resource Allocation' and 'Mental Fatigue Score'
   - All numerical features are normalized using MinMaxScaler

## 📈 Key Results & Findings

### Model Performance Comparison
| Model | RMSE | R² Score |
|-------|------|----------|
| Linear Regression | 0.0748 | 0.8480 |
| Decision Tree | 0.0660 | 0.8814 |
| Random Forest | 0.0624 | 0.8945 |
| **Gradient Boosting** | **0.0602** | **0.9050** |

### Optimized Model Performance
- **Best Model**: Gradient Boosting Regressor
- **Final RMSE**: 0.0589
- **Final R² Score**: 0.9090
- **Best Parameters**: 
  - learning_rate: 0.2
  - max_depth: 4
  - n_estimators: 100
  - min_samples_leaf: 2
  - min_samples_split: 5

### Key Insights
1. **Mental Fatigue Score** shows strong correlation with burnout rates
2. **Resource Allocation** (working hours) significantly impacts burnout
3. **Company Type** and **WFH Setup** availability influence burnout levels
4. The model achieved **90.9% accuracy** in predicting burnout rates

## 📁 File Structure
```
Capstone 3/
├── README.md                 # This file
├── task.ipynb               # Project requirements and instructions
├── capstone_3 (1).ipynb     # Main analysis and modeling notebook
└── data/                    # Data files (loaded from Google Drive)
    ├── train.csv
    └── test.csv
```

## 🎯 Business Impact & Recommendations

### For HR Teams:
1. **Monitor Mental Fatigue Scores** regularly through surveys
2. **Optimize Resource Allocation** to prevent overwork
3. **Improve WFH Infrastructure** for remote employees
4. **Early Intervention** for employees with high predicted burnout risk

### For Organizations:
- Implement predictive monitoring systems
- Create wellness programs targeting high-risk employees
- Establish work-life balance policies
- Regular employee engagement assessments

## 🔮 Future Enhancements
- Include additional features (manager feedback, project complexity)
- Implement real-time prediction dashboard
- Develop intervention recommendation system
- Cross-industry model validation

## 📚 Learning Outcomes
This capstone project demonstrates:
- End-to-end machine learning pipeline development
- Real-world data preprocessing challenges
- Model comparison and optimization techniques
- Business insight generation from predictive models

---

**Note**: This is an educational capstone project for the 3MTT program, simulating a real-world business scenario for learning purposes.