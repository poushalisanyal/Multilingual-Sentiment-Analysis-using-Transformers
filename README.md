# Multilingual-Sentiment-Analysis-using-Transformers
This project focuses on multilingual sentiment analysis using the Dhruv Multilingual Sentiment Analysis Dataset. The goal was to extract sentiments from text written in multiple languages and to understand how different transformer models perform on multilingual data.


Objective: 
Perform sentiment classification on multilingual text
Compare the performance of BERT and XLM-RoBERTa
Analyze the impact of model selection on multilingual NLP tasks


Dataset:
Name: Dhruv Multilingual Sentiment Analysis Dataset
Source: Hugging Face
Description:
The dataset contains sentiment-labeled text across multiple languages, mainly focused on Indic languages. Each text sample is labeled as Positive, Neutral, or Negative, making it suitable for sentiment classification tasks.


Methodology:
1. Data Preparation
Loaded the dataset using Hugging Face datasets
Filtered valid sentiment labels
Mapped textual labels to numerical values
Split the data into training and evaluation sets
2. Model Training
Baseline Model: BERT
Improved Model: XLM-RoBERTa
Used Hugging Face Trainer API for fine-tuning
Tokenized text using the respective model tokenizers
3. Evaluation
Evaluated model performance using accuracy
Compared results across both models


Results:
Model	Accuracy= BERT	~63%
                XLM-RoBERTa	82%

Observation:
XLM-RoBERTa performed significantly better due to its multilingual pretraining on large-scale multilingual corpora, making it more suitable for handling diverse languages compared to BERT.


Tools & Technologies:
Python
Hugging Face Transformers
Hugging Face Datasets
BERT
XLM-RoBERTa
NLP


Key Learnings:
Model selection plays a crucial role in multilingual NLP tasks.

Models trained primarily on English data may underperform on multilingual datasets

XLM-RoBERTa is better suited for multilingual sentiment analysis due to its training strategy and language coverage
