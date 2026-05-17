# Part 3 – NLP and Sequence Modeling Mini Project

This project builds a complete NLP pipeline using a customer support dataset.  
The goal is to compare traditional text‑vectorization models with sequence‑based deep learning models such as LSTMs.

---

## 📁 Dataset

File: `customer_support_text_classification.csv`

Columns include:
- `ticket_id`
- `channel`
- `customer_message`
- `sentiment_label` (negative, neutral, positive)
- `word_count`
- `urgent_flag`

---

## 📌 Task Overview

### **Task 1 — Dataset Understanding**
- Loaded dataset using pandas  
- Displayed:
  - Number of records  
  - Unique sentiment labels  
  - Sample messages  
  - Average text length  
  - Class distribution (bar plot)

---

### **Task 2 — Text Preprocessing**
Performed text cleaning:
- Lowercasing  
- Removing digits, punctuation, and ticket numbers  
- Tokenization  
- Optional stopword removal  
- Tokenizer + padded sequences for LSTM models  
- Created `clean_text` column  

---

### **Task 3 — Text Vectorization**
Two approaches were used:
1. **TF‑IDF (unigrams + bigrams)** for baseline ML  
2. **Tokenizer integer sequences** for LSTM  

Vectorization is required because machine learning models operate on numerical tensors, not raw text.

---

### **Task 4 — Baseline Model**
Model: **Logistic Regression + TF‑IDF**

Evaluation:
- Accuracy  
- Precision, Recall, F1‑score  
- Confusion matrix (saved as `results/model_evaluation.png`)

---

### **Task 5 — Sequence Model (LSTM)**
Built a simple LSTM architecture:

- Embedding layer (100 dimensions)  
- LSTM (64 units)  
- Dense layer (ReLU)  
- Output softmax layer (3 classes)  

Trained for a few epochs and evaluated on the test set.  
Saved accuracy plot as `results/lstm_accuracy.png`.

---

### **Task 6 — Attention & Transformer Reflection**
Included a conceptual explanation of:
- RNN limitations  
- How LSTMs improve long‑term memory  
- Why attention mechanisms matter  
- Why transformers dominate modern NLP  

---

## 📂 Repository Structure

part-3-nlp-sequence-modeling/
│
├── README.md
├── notebook.ipynb
├── requirements.txt
└── results/
  ├── model_evaluation.png
  └── sample_predictions.txt

---

## 🚀 Summary

This project demonstrates the full NLP workflow:
- Data exploration  
- Preprocessing  
- Vectorization  
- Baseline ML  
- Deep learning sequence modeling  
- Reflection on modern NLP architectures  

It provides a strong foundation for understanding how text is transformed into numerical form and how different models process language.
