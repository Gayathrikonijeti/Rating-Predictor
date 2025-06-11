# ⭐ Rating Predictor

This project predicts the sentiment or rating of Amazon product reviews using two approaches:
1. **Machine Learning** with a **Random Forest Classifier**
2. **Rule-based Sentiment Analysis** using **VADER (Valence Aware Dictionary and sEntiment Reasoner)**
---

## 📖 Overview

Text reviews provide valuable insights into customer opinions. This project classifies reviews into sentiments (**Positive**, **Neutral**, **Negative**) by:
- Training a machine learning model (Random Forest) on labeled review text
- Applying VADER sentiment scores as an alternative or supplementary method

---

## 📂 Dataset

- **Source**: `amazon_data.csv`
- **Columns** include review texts and numeric ratings.
- Ratings are mapped as:
  - `4, 5` → Positive  
  - `3` → Neutral  
  - `1, 2` → Negative  

---

## 🧰 Technologies Used

- Python (Jupyter Notebook)
- Pandas, NumPy
- Matplotlib, Seaborn
- NLTK (for VADER)
- Scikit-learn (Random Forest, TF-IDF, Evaluation Metrics)

---

## 🧠 Approaches

### 1️⃣ Machine Learning: Random Forest
- **Text Preprocessing**:
  - Lowercasing, punctuation & stopword removal, stemming
- **Feature Extraction**:
  - TF-IDF vectorization
- **Model**: RandomForestClassifier
- **Evaluation**: Accuracy Score, Confusion Matrix

### 2️⃣ Sentiment Analysis: VADER
- Applied directly to raw review text
- Generates compound sentiment scores
- Classifies based on thresholds:
  - `compound >= 0.05` → Positive
  - `compound <= -0.05` → Negative
  - else → Neutral
