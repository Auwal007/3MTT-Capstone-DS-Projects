# Delivery Delay Prediction - Capstone Project 4

## 🎯 Project Objective

This capstone project focuses on optimizing logistics and supply chain operations by predicting delivery delays using machine learning. As part of the 3MTT (3 Million Technical Talent) program, this project simulates working as a data scientist for SwiftChain Analytics to solve one of the most challenging problems in supply chain management.

**Goal**: Develop a predictive model to classify delivery outcomes and provide actionable insights to reduce delivery delays and enhance operational efficiency.

## 📋 Problem Statement

Delivery delays are a critical challenge in supply chain management, impacting:
- Customer satisfaction and retention
- Operational costs and efficiency
- Company reputation and competitiveness
- Revenue and business growth

This project aims to:
- Analyze logistics data to identify delay patterns
- Build machine learning models to predict delivery status
- Generate actionable recommendations for logistics optimization

## 🛠️ Approach & Methodology

### Phase 1: Problem Understanding
- Analyzed business impact of delivery delays
- Examined key variables in the logistics dataset

### Phase 2: Exploratory Data Analysis (EDA)
- Data structure inspection and quality assessment
- Statistical analysis of numerical and categorical variables
- Visualization of shipping mode vs. delivery status relationships
- Missing value identification and handling strategies

### Phase 3: Data Preprocessing & Feature Engineering
- **Data Cleaning**: Removed irrelevant columns (IDs, duplicates)
- **Outlier Handling**: Applied 5th-95th percentile capping for critical numerical features
- **Feature Scaling**: Standardized numerical features using StandardScaler
- **Categorical Encoding**: 
  - Label encoding for ordinal features
  - One-hot encoding for nominal features
  - Frequency encoding for high-cardinality features
- **Feature Creation**:
  - `shipping_duration`: Days between order and shipping dates
  - `effective_price`: Price after discount calculations
  - `items_per_order`: Total items per order
  - `order_month` & `order_weekday`: Temporal features

### Phase 4: Model Development
- **Data Balancing**: Applied SMOTE for class imbalance handling
- **Algorithms Tested**:
  - Logistic Regression (with class balancing)
  - Random Forest Classifier
  - XGBoost Classifier
- **Hyperparameter Optimization**: Used Optuna for XGBoost tuning
- **Cross-validation**: 5-fold stratified cross-validation

## 📊 Dataset Information

**Target Variable**: 
- `-1`: Early delivery
- `0`: On-time delivery  
- `1`: Late delivery

**Key Features** (41 total variables):
| Category | Examples |
|----------|----------|
| Customer Data | customer_segment, customer_city, customer_country |
| Order Details | order_date, payment_type, order_item_quantity |
| Product Info | category_name, product_price, department_name |
| Shipping | shipping_mode, shipping_date, market |
| Financial | profit_per_order, sales_per_customer, order_item_discount |

## 🚀 How to Reproduce Results

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn optuna
```

### Step-by-Step Instructions

1. **Setup Environment**
   ```bash
   # Navigate to the Capstone 4 directory
   cd "Capstone 4"
   ```

2. **Open the Jupyter Notebook**
   ```bash
   jupyter notebook "Capstone_4 (1).ipynb"
   ```

3. **Execute Phases Sequentially**:
   - **Phase 1**: Problem understanding and business impact analysis
   - **Phase 2**: EDA with visualizations and data insights
   - **Phase 3**: Data preprocessing and feature engineering
   - **Phase 4**: Model training and evaluation
   - **Phase 5**: Model optimization and feature importance analysis

4. **Key Execution Notes**:
   - Ensure internet connection for Google Drive data loading
   - Dataset contains 41 features across multiple categories
   - SMOTE is applied to handle class imbalance
   - Optuna optimization may take time depending on n_trials setting

## 📈 Key Results & Findings

### Model Performance Comparison
| Model | Accuracy | F1 Score (Macro) | Notes |
|-------|----------|------------------|--------|
| Logistic Regression | ~0.65 | ~0.40 | Baseline with class balancing |
| Random Forest | ~0.85 | ~0.60 | Good performance on balanced data |
| **XGBoost (Optimized)** | **~0.87** | **~0.65** | **Best performing model** |

### Key Insights from Analysis

1. **Shipping Mode Impact**:
   - Standard Class has highest percentage of late deliveries
   - Same Day and First Class show most reliable performance

2. **Geographical Factors**:
   - Delivery performance varies significantly by region
   - Certain customer cities/states show higher delay rates

3. **Feature Importance** (Top Contributors):
   - Shipping mode and duration
   - Geographical features (region, city frequency)
   - Order characteristics (items per order, effective price)
   - Customer segment information

### Class Distribution Insights
- **Original Dataset**: Heavily imbalanced toward on-time deliveries
- **After SMOTE**: Balanced distribution improved model performance
- **Business Impact**: Most delays occur in Standard Class shipping

## 📁 File Structure
```
Capstone 4/
├── README.md                    # This file
├── task.ipynb                   # Project requirements and instructions
├── Capstone_4 (1).ipynb        # Main analysis and modeling notebook
└── data/                        # Data files (loaded from Google Drive)
    ├── logistics.csv
    └── feature_description.csv
```

## 🎯 Business Recommendations

### Immediate Actions:
1. **Optimize Standard Class Logistics**: Focus on improving Standard Class shipping reliability
2. **Regional Analysis**: Identify and address high-risk delivery regions
3. **Customer Segment Strategy**: Develop targeted approaches for delay-prone segments
4. **Predictive Integration**: Implement model for real-time delay prediction

### Strategic Improvements:
- Establish regional distribution centers in high-delay areas
- Partner with more reliable carriers for Standard Class
- Proactive customer communication for high-risk orders
- Continuous monitoring and model retraining

## 🔮 Future Enhancements
- Real-time delay prediction dashboard
- Advanced feature engineering (weather data, traffic patterns)
- Deep learning models for sequential pattern recognition
- Multi-objective optimization (cost vs. delivery time)

## 📚 Learning Outcomes
This capstone project demonstrates:
- End-to-end machine learning pipeline for logistics optimization
- Advanced data preprocessing and feature engineering techniques
- Class imbalance handling in real-world scenarios
- Business insight generation from predictive models
- Hyperparameter optimization using modern tools (Optuna)

## 🔍 Model Evaluation Metrics
- **Primary**: F1 Score (macro) - accounts for class imbalance
- **Secondary**: Accuracy - overall prediction correctness
- **Business**: Focus on reducing false negatives (missed delay predictions)

---

**Note**: This is an educational capstone project for the 3MTT program, simulating real-world logistics optimization challenges for learning purposes.