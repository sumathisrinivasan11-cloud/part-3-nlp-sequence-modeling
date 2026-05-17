
---

## 📝 Dataset

The dataset contains customer support messages with the following fields:

- `ticket_id`
- `channel`
- `customer_message`
- `sentiment_label`
- `word_count`
- `urgent_flag`

Example entries include messages such as:

- “The refund process was fast and convenient.”  
- “My refund is still pending and this experience is frustrating.”  
- “I need help finding the invoice for my last order.”

---

## ✅ Task 1 — Dataset Understanding

The notebook includes:

- Number of records  
- Unique sentiment classes  
- Sample messages  
- Average text length  
- Class distribution visualization  

---

## 🧹 Task 2 — Text Preprocessing

Preprocessing steps:

- Lowercasing  
- Removing special characters  
- Tokenization  
- Stopword removal  
- Padding sequences (for LSTM model)

---

## 🔡 Task 3 — Text Vectorization

Two approaches are implemented:

### **1. TF‑IDF Vectorization**
Used for the baseline machine learning model.

### **2. Tokenizer + Sequences**
Used for the LSTM deep learning model.

**Why vectorization?**  
Machine learning models cannot understand raw text.  
Vectorization converts text into numerical form so models can learn patterns.

---

## 📊 Task 4 — Baseline Model

A simple baseline classifier is built using:

- **TF‑IDF vectorizer**
- **Logistic Regression**

Evaluation includes:

- Accuracy  
- Precision, Recall, F1-score  
- Confusion matrix  

This serves as a benchmark before using sequence models.

---

## 🔁 Task 5 — Sequence Model (LSTM)

A deep learning model is implemented using:

- Embedding layer  
- LSTM layer  
- Dense output layer  

Training includes:

- Sparse categorical crossentropy loss  
- Adam optimizer  
- Accuracy metric  

The notebook compares LSTM performance with the baseline model.

---

## 🧠 Task 6 — Attention & Transformer Reflection

The notebook includes explanations of:

- Why RNNs struggle with long-term dependencies  
- How LSTMs improve memory handling  
- What attention mechanisms solve  
- Why transformers dominate modern NLP and Generative AI  

---

## 📦 Results

The `results/` folder contains:

- Model evaluation outputs  
- Sample predictions from the baseline model  

---

## 🚀 How to Run

1. Install dependencies:pip install -r requirements.txt
2. Open the notebook:jupyter notebook notebook.ipynb
3. Run all cells in order.

---

## ✨ Summary

This project demonstrates:

- End‑to‑end NLP workflow  
- Traditional vs. deep learning text modeling  
- Practical understanding of embeddings, LSTMs, and attention  

It forms a strong foundation for more advanced NLP tasks such as transformers and large language models.


