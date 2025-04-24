# Hate Speech Classification on Twitter (English and Arabic)

## Overview

This project classifies hate speech in Twitter posts.  
It works on two datasets:

- English tweets  
- Arabic tweets

Each dataset is preprocessed, trained, and evaluated.  
The goal is to detect hate speech in both languages using NLP techniques and machine learning models.

---

## Objectives

- Preprocess English and Arabic Twitter data  
- Train separate models for each language  
  
---

## Datasets

- `data/english_tweets.csv`  
- `data/arabic_tweets.csv`

Each file contains:

- `id`  
- `tweet`  
- `label` (Hate or Non-Hate)

---

## Preprocessing

### English

- Lowercasing  
- Remove URLs, mentions, punctuation  
- Tokenization  
- Stopword removal  
- Lemmatization

### Arabic

- Normalize text   
- Remove URLs, mentions, punctuation    
- Stopword removal
  
---

## Feature Extraction

- **TF-IDF**  
  - Unigram and bigram features  
  - Used with classical models (Logistic regression)

- **Word Embeddings**  
  - **GloVe**  
  - **Word2Vec**  
  - **FastText**
  
- **1D CNN**  
  - Used on top of embedding layers  
  - Captures local n-gram patterns in the tweet sequence

- **RNN**  
  - Captures sequential dependencies in text  
  - Suitable for modeling time-series or sequence-based data

- **LSTM**  
  - Long Short-Term Memory  
  - Overcomes RNN’s vanishing gradient problem  
  - Better at capturing long-range dependencies

- **GRU**  
  - Gated Recurrent Unit  
  - Similar to LSTM but with a simpler architecture  
  - Fewer parameters and faster to train

- **Unidirectional LSTM, GRU**  
  - Process text in one direction (usually left-to-right)  
  - Suitable when past context is more important than future context

- **Bidirectional LSTM, GRU**  
  - Processes text in both directions (left-to-right and right-to-left)  
  - Captures both past and future context for each time step in the sequence


---

## Evaluation

Each model is evaluated using:

- Accuracy  
- Precision  
- Recall  
- F1-Score  
- Confusion Matrix

