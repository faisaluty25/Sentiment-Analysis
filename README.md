📝 Arabic Text Classification with NLP & ML
This project focuses on building a text classification model for Arabic text using NLP preprocessing and a machine learning pipeline. The goal is to predict sentiment (or rating) based on user-written Arabic reviews.

📁 Dataset
The dataset contains the following columns:

review_description: Arabic text (user reviews)

rating: Target label (e.g., rating or sentiment)

company: The company associated with the review

🧠 Project Workflow
1. Data Preprocessing
Normalization using regex:

Remove diacritics and Tatweel

Unify characters (e.g., أ, إ, آ → ا)

Remove repeated characters

Tokenization of Arabic text

Stopwords removal using a custom stopword list

Stemming using SnowballStemmer

Rejoining tokens into clean strings for vectorization

2. Feature Extraction
TF-IDF Vectorization applied to the cleaned text

3. Data Splitting
Two approaches used:

Train/Validation/Test split

K-Fold Cross-Validation (5-fold)

4. Model Building
Logistic Regression used as baseline classifier

Evaluated using:

Accuracy

Confusion Matrix

Classification Report

🔍 Evaluation & Insights
Both evaluation strategies (split & cross-validation) were compared to ensure consistency in model performance. Performance metrics across validation and test sets were close — indicating a well-generalized model.

📚 Technologies Used
Python

pandas, numpy – for data handling

regex (re) – for Arabic text normalization

nltk – SnowballStemmer

scikit-learn – modeling, vectorization, evaluation


🚀 Future Improvements
Try other models (e.g., SVM, XGBoost, transformers)

Use deep learning for better semantic understanding

Fine-tune Arabic pre-trained models (e.g., AraBERT)

Expand and balance the dataset if needed

🙌 Acknowledgements
Thanks to the authors of open-source Arabic NLP libraries and the dataset providers.

