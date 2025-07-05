# Fake News Detection - Capstone Project 2

## 🎯 Project Objective

This capstone project focuses on detecting fake news using natural language processing and machine learning techniques. As part of the 3MTT (3 Million Technical Talent) program, this project demonstrates practical application of text classification methods for identifying misinformation.

**Goal**: Build and evaluate machine learning models to classify news articles as fake or real while gaining hands-on experience with NLP techniques and text data processing.

## 📊 Dataset

- **Size**: 12,999 news posts from 244 websites
- **Features**: Text content, timestamps, URLs, domain information
- **Labels**: Binary classification (fake vs. real news)
- **Source**: Automatically downloaded from Google Drive in the notebook

## 🛠️ Methodology

### Data Preprocessing
- Text cleaning (lowercasing, special character removal, stopword removal)
- Missing value handling
- Basic feature extraction (word count, sentiment analysis)

### Feature Engineering
- **TF-IDF Vectorization**: 5,000 text features for classification
- **Sentiment Analysis**: VADER sentiment scores
- **Temporal Features**: Publication time patterns
- **Domain Analysis**: Website source indicators

### Model Development
- **Algorithms**: Logistic Regression and Linear SVC
- **Data Split**: 75/25 train-test split with stratified sampling
- **Evaluation**: Accuracy, precision, recall, and F1-score metrics

## 📈 Results

### Model Performance
- **Logistic Regression**: 88.31% accuracy, 78.54% precision
- **Linear SVC**: 88.40% accuracy, 78.15% precision
- **F1-Scores**: Both models achieved ~83% F1-score

### Key Learning Insights
1. **TF-IDF Features**: Most effective for text classification
2. **Sentiment Analysis**: Provided additional classification power
3. **Model Comparison**: Both algorithms performed similarly well
4. **Feature Engineering**: Critical for improving model performance

## 🚀 How to Reproduce Results

### Prerequisites
```bash
pip install pandas numpy scikit-learn nltk matplotlib seaborn wordcloud
```

### NLTK Setup
```python
import nltk
nltk.download('stopwords')
nltk.download('punkt')
nltk.download('vader_lexicon')
```

### Step-by-Step Instructions
1. **Run the Notebook**
   ```bash
   jupyter notebook "Capston_2.ipynb"
   ```
2. **Execute all cells** sequentially from top to bottom
3. **Dataset downloads** automatically from Google Drive
4. **Runtime**: Approximately 10-15 minutes for complete execution

## 📁 Project Structure
```
Capstone 2/
├── README.md           # Project documentation
├── Capston_2.ipynb     # Main analysis notebook
└── task.ipynb          # Project requirements
```

## 📚 Learning Outcomes

This capstone project demonstrates:
- **Text Preprocessing**: Cleaning and preparing text data for analysis
- **Feature Engineering**: Converting text to numerical features using TF-IDF
- **NLP Techniques**: Sentiment analysis and text classification methods
- **Model Evaluation**: Comparing classification algorithms and interpreting results
- **Data Visualization**: Creating meaningful plots and confusion matrices

## 🔮 Future Enhancements
- Experiment with deep learning models (LSTM, BERT)
- Implement advanced feature selection techniques
- Explore ensemble methods for better performance
- Add cross-validation for more robust evaluation

---

**Note**: This is an educational capstone project for the 3MTT program, demonstrating NLP and machine learning concepts for text classification in the context of misinformation detection.
