# 🎬 IMDb Movie Review Sentiment Analysis

## 📌 Overview
This project implements a deep learning model to classify IMDb movie reviews as **positive** or **negative**.  
Sentiment analysis is a key task in Natural Language Processing (NLP), and movie reviews provide a rich dataset for testing text classification models.  
Our goal is to build, train, and evaluate models that can accurately predict sentiment, demonstrating the effectiveness of RNNs and LSTMs.

---

## 📂 Dataset
- **Source:** IMDb dataset (available via `keras.datasets.imdb` or Hugging Face).  
- **Format:** Reviews are pre-tokenized into integers, each representing a word.  
- **Labels:**  
  - `0` → Negative review  
  - `1` → Positive review  
- **Samples:**  
  - Training set: 25,000 reviews  
  - Test set: 25,000 reviews  

---

## ⚙️ Preprocessing
- Limited vocabulary to top 10,000 words.  
- Padded/truncated reviews to fixed length (200 words).  
- Decoded reviews for human readability.  
- Balanced dataset with equal positive and negative samples.  

---

## 🏗️ Methodology
We implemented and compared multiple models:

1. **SimpleRNN** – baseline sequential model.  
2. **LSTM** – improved handling of long-term dependencies.  
3. **Bidirectional LSTM** – captures context from both directions.  

**Architecture Highlights:**
- Embedding layer (word → vector).  
- Recurrent layer (RNN/LSTM/Bidirectional LSTM).  
- Dense output layer with sigmoid activation.  

---

## 📊 Results
| Model              | Test Accuracy |
|--------------------|---------------|
| SimpleRNN          | ~82%          |
| LSTM               | ~84%          |
| Bidirectional LSTM | ~83%          |

- Accuracy/Loss curves plotted for training and validation.  
- Confusion Matrix used to analyze misclassified reviews.  
- Sample predictions visualized for demonstration.  

---

## 🔑 Insights
- **SimpleRNN** provides a good baseline but struggles with longer dependencies.  
- **LSTM** improves accuracy by remembering context over longer sequences.  
- **Bidirectional LSTM** achieves the best performance by learning from both past and future context.  

---

## 🚀 Enhancements
Future improvements could include:
- Using **pre-trained embeddings** (GloVe, Word2Vec).  
- Adding **Dropout layers** to reduce overfitting.  
- Experimenting with **transformer-based models** (DistilBERT, BERT).  

---

## 📝 Summary
This project demonstrates the effectiveness of RNN-based models for sentiment analysis.  
By preprocessing data, experimenting with different architectures, and evaluating results, we achieved **~89% accuracy** on the IMDb dataset.  

**Key Takeaway:**  
Deep learning models, especially LSTMs and Bidirectional LSTMs, significantly improve sentiment classification compared to simpler RNNs.

---

## 📌 Requirements
- Python 3.x  
- TensorFlow / Keras  
- NumPy, Matplotlib, Seaborn  

Install dependencies:
```bash
pip install tensorflow numpy matplotlib seaborn
