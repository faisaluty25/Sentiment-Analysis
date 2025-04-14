# 📝 Arabic Text Classification with NLP & ML

This project focuses on building a text classification model for **Arabic text** using NLP preprocessing and a machine learning pipeline. The goal is to predict **sentiment** (or **rating**) based on user-written Arabic reviews.

---

## 📁 Dataset

The dataset contains the following columns:

- `review_description`: Arabic text (user reviews)
- `rating`: Target label (e.g., rating or sentiment)
- `company`: The company associated with the review

---

## 🧠 Project Workflow

### 1. Data Preprocessing

- **Normalization using regex**:
  - Remove diacritics and Tatweel
  - Unify characters (e.g., `أ`, `إ`, `آ` → `ا`)
  - Remove repeated characters

- **Tokenization** of Arabic text  
- **Stopwords removal** using a custom Arabic stopword list  
- **Stemming** using `SnowballStemmer` or `FarasaStemmer`  
- **Rejoining tokens** into clean strings for vectorization

---

### 2. Feature Extraction

- **TF-IDF Vectorization** applied to the cleaned Arabic text

---

### 3. Data Splitting

Two approaches were used:

- **Train / Validation / Test split**
- **K-Fold Cross-Validation (5 folds)**

---

### 4. Model Building

- **Model**: Logistic Regression (baseline)
- **Evaluation Metrics**:
  - Accuracy
  - F1-Score
  - Confusion Matrix
  - Classification Report

---

## 🔍 Evaluation & Insights

Both evaluation strategies (split and cross-validation) were compared to ensure consistency in model performance.  
**Validation and test metrics were close**, indicating a **well-generalized model**.

### ✅ **Validation Results**
          precision    recall  f1-score   support

      -1       0.88      0.89      0.89      3629
       0       0.92      0.85      0.88      3826
       1       0.82      0.89      0.85      3285

accuracy                           0.87     10740


### ✅ **Test Results**
          precision    recall  f1-score   support

      -1       0.88      0.89      0.88      4680
       0       0.93      0.85      0.88      4710
       1       0.82      0.88      0.85      4035

accuracy                           0.87     13425
