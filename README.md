# Multilingual Sentiment Analysis

This project presents a multilingual sentiment analysis system built using transformer-based models. The objective is to classify text into sentiment categories (positive, negative, neutral) across multiple languages and evaluate how well different models generalize in cross-lingual settings.

# Overview

The project explores the effectiveness of transformer models in handling multilingual data. Multiple models were fine-tuned and evaluated not only on standard datasets but also on unseen languages such as Japanese and Chinese to test real-world applicability.

# Models Used
XLM-RoBERTa-base
BERT
CardiffNLP Twitter RoBERTa

# Cross-Lingual Evaluation
To evaluate generalization, the models were tested on:
Japanese dataset
Chinese dataset
These datasets were not part of the primary training distribution, making the evaluation truly cross-lingual.

# Comparative Results
XLM-RoBERTa
Test Accuracy: 0.6991
Precision: 0.7046
Recall: 0.6991
F1-score: 0.7002

Japanese Test F1: 0.5552
Chinese Test F1: 0.5670

BERT
Test Accuracy: 0.6378
Precision: 0.6432
Recall: 0.6378
F1-score: 0.6392

Japanese Test F1: 0.4233
Chinese Test F1: 0.5080

Cardiff NLP RoBERTa
Test Accuracy: 0.6159
Precision: 0.6155
Recall: 0.6159
F1-score: 0.6155

Japanese Test F1: 0.2820
Chinese Test F1: 0.3162

# Key Findings
XLM-RoBERTa achieved the best performance across all datasets
Multilingual pretraining significantly improves cross-lingual generalization
Models trained primarily on English data perform poorly on other languages
Performance drops in unseen languages highlight the challenges of multilingual NLP

# Methodology
Data preprocessing (cleaning, normalization, tokenization)
Tokenization using model-specific tokenizers
Fine-tuning transformer models
Evaluation using Accuracy, Precision, Recall, and F1-score

# Challenges
Handling multiple scripts (English, Japanese, Chinese)
Dataset imbalance across languages
Generalization to unseen linguistic structures
