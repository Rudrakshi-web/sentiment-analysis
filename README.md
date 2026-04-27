# Sentiment Analysis on IMDB Dataset

This project focuses on building a sentiment classification system for movie reviews using different Natural Language Processing (NLP) techniques and machine learning models. The objective is to compare various text representations and evaluate their performance on a binary classification task (positive vs negative sentiment).

## Dataset

The dataset used is the IMDB movie reviews dataset, which contains labeled reviews as either positive or negative. It is a balanced dataset and commonly used for benchmarking sentiment analysis models.

## Approach

### 1. Text Preprocessing

Before training the models, the raw text data was cleaned and processed using the following steps:

- Removal of HTML tags  
- Removal of punctuation and special characters  
- Conversion to lowercase  
- Tokenization using NLTK  
- Removal of English stopwords  

This step ensures that the input text is standardized and noise is reduced.

---

### 2. Feature Extraction

Different methods were used to convert text into numerical representations:

- **TF-IDF (Term Frequency–Inverse Document Frequency)**  
  Captures word importance based on frequency and rarity.

- **Universal Sentence Encoder (USE)**  
  Generates dense vector representations capturing semantic meaning of sentences.

- **TF-IDF + USE (Combined Features)**  
  Combines sparse and dense representations to improve performance.

- **BERT Embeddings**  
  Uses transformer-based contextual embeddings for deeper understanding of text.

---

### 3. Models Used

The following machine learning models were implemented and compared:

- Logistic Regression  
- Support Vector Machine (SVM)  
- Naive Bayes  
- XGBoost  
- Random Forest  

Logistic Regression consistently performed well across different feature types.

---

## Results

The models were evaluated using a train-test split (80-20). The following results were obtained:

| Model | Accuracy |
|------|---------|
| TF-IDF (Logistic Regression) | 88.8% |
| USE (Logistic Regression) | 83.0% |
| TF-IDF + USE | 88.5% |
| BERT | 86.3% |

---

## Evaluation Metrics

Performance was evaluated using standard classification metrics:

- Accuracy  
- Precision  
- Recall  
- F1-score  
- Confusion Matrix  

These metrics provide a balanced view of model performance, especially for classification tasks.

---

## Observations

- TF-IDF with Logistic Regression achieved the highest accuracy and overall balanced performance.  
- USE embeddings captured semantic meaning but resulted in slightly lower accuracy.  
- Combining TF-IDF and USE improved feature richness but did not significantly outperform TF-IDF alone.  
- BERT performed well, especially in recall, indicating better understanding of context.  

---

## Conclusion

Traditional methods like TF-IDF combined with Logistic Regression remain strong baselines for sentiment analysis tasks. While deep learning models like BERT provide better contextual understanding, they do not always outperform simpler models on this dataset without further tuning.

---

## Future Improvements

- Hyperparameter tuning for all models  
- Fine-tuning BERT for improved performance  
- Testing other transformer-based models  
- Deploying the model using a web interface (e.g., Streamlit)  
