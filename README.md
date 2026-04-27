# 📰 Fake News Detection using NLP

## 📌 Project Overview
This project focuses on building a machine learning model to classify news articles as **Fake** or **Real** using Natural Language Processing (NLP) techniques. The goal is to analyze textual patterns and linguistic features to detect misinformation.

---

## 🚀 Key Highlights
- Built an end-to-end NLP pipeline for text classification
- Achieved **98.7% Accuracy** and **99.8% ROC-AUC**
- Implemented **TF-IDF vectorization with bi-grams**
- Compared multiple models (Logistic Regression vs Naive Bayes)
- Performed **feature importance analysis** and **error analysis**

---

## 📊 Dataset
- Source: Kaggle (Fake and Real News Dataset)
- Total Samples: ~44,800
- Balanced dataset with equal distribution of fake and real news
- Features:
  - Title
  - Text
  - Subject
  - Date

---

## 🧹 Data Preprocessing
- Combined **title and text** into a single feature
- Converted text to lowercase
- Removed punctuation, numbers, and special characters
- Tokenized text into words
- Removed stopwords
- Applied stemming for normalization

---

## 🔢 Feature Engineering
Used **TF-IDF Vectorization** to convert text into numerical features:
- `max_features = 5000`
- `ngram_range = (1,2)` (unigrams + bigrams)
- `min_df = 5` (remove rare words)
- `max_df = 0.7` (remove overly common words)

---

## 🤖 Models Used

### 1. Logistic Regression
- Best performing model
- Accuracy: **98.7%**
- ROC-AUC: **99.8%**

### 2. Naive Bayes
- Faster but less accurate
- Accuracy: **~92%**
- ROC-AUC: **~97.8%**

---

## 📈 Model Evaluation

- Evaluated using:
  - Accuracy
  - Precision, Recall, F1-score
  - ROC-AUC Score
- Logistic Regression outperformed Naive Bayes due to its ability to capture feature relationships

---

## 🔍 Key Insights

- Fake news often contains:
  - Informal language
  - Sensational phrases
  - Social media-style references (e.g., "video", "read")

- Real news often includes:
  - Source attribution (e.g., "Reuters")
  - Locations (e.g., "Washington")
  - Timestamps (e.g., "Tuesday")

- Model effectively captures **writing style and credibility patterns**, not just keywords

---

## ⚠️ Limitations

- Dataset bias observed (e.g., presence of "Reuters" in real news)
- Model may not generalize well to unseen sources
- High accuracy due to structured dataset; real-world performance may vary

---

## 📉 Error Analysis

- False Positives (Fake → Real): 72
- False Negatives (Real → Fake): 42

- Model is slightly biased toward predicting news as real
- Fake news that mimics formal journalism is harder to detect

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- NLTK

---

## 📌 Future Improvements

- Replace stemming with lemmatization
- Try advanced models (SVM, XGBoost)
- Implement deep learning models (LSTM, BERT)
- Deploy using Streamlit or Flask

---
