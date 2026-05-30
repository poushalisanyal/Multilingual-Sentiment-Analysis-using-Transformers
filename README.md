# Cross-Lingual Sentiment Analysis using XLM-RoBERTa

## Overview

This project focuses on Cross-Lingual Sentiment Analysis, where a model is trained on multiple languages and evaluated on completely unseen languages to measure its ability to transfer sentiment knowledge across linguistic boundaries.

The goal was to investigate whether multilingual transformer models can understand sentiment consistently across different languages without relying on machine translation.

---

## Dataset

The multilingual dataset contains text samples labeled as:

* Positive
* Negative
* Neutral

### Training Languages

The model was trained and evaluated on the following 9 languages:

* English
* Hindi
* Arabic
* French
* German
* Italian
* Portuguese
* Spanish
* Indonesian
* Malay

### Cross-Lingual Evaluation Languages

To evaluate true cross-lingual generalization, the model was tested on languages that were never used during training:

* Chinese
* Japanese

This setup allows us to measure zero-shot cross-lingual sentiment transfer.

---

## Problem Statement

Traditional sentiment analysis models often struggle when applied to languages different from those seen during training.

Key challenges include:

* Different writing systems and scripts
* Language-specific grammar structures
* Cultural and contextual variations
* Limited labeled data for many languages
* Loss of information during machine translation

This project explores whether multilingual transformer models can overcome these challenges through shared multilingual representations.

---

## Models Compared

### Traditional Machine Learning Models

* Naive Bayes
* Logistic Regression
* Support Vector Machine (SVM)

These models use TF-IDF features as text representations.

### Transformer-Based Models

* mBERT
* Cardiff NLP
* XLM-RoBERTa

---

## Final Model

After comparing multiple approaches, XLM-RoBERTa was selected as the primary model because of its strong multilingual capabilities and superior performance across languages.

The model was fine-tuned for 3-class sentiment classification:

* Positive
* Negative
* Neutral

---

## Project Pipeline

1. Data Collection
2. Text Cleaning and Preprocessing
3. Unicode Normalization
4. Removal of URLs and User Mentions
5. Tokenization
6. Feature Extraction
7. Model Training
8. Evaluation
9. Cross-Lingual Testing

---

## Results

### Traditional Models

* Naive Bayes
* Logistic Regression
* SVM

These models provided useful baselines but struggled to capture multilingual semantic relationships.

### Transformer Models

Among all evaluated models, XLM-RoBERTa achieved the strongest overall performance.

Key observations:

* Highest performance on multilingual sentiment classification
* Strong generalization across language families
* Successful zero-shot transfer to Chinese and Japanese
* Significant improvement over traditional ML approaches

---

## Key Findings

* Multilingual transformers outperform traditional TF-IDF based models.
* Shared multilingual representations help transfer sentiment knowledge across languages.
* XLM-RoBERTa successfully classified sentiment in Chinese and Japanese despite never seeing these languages during training.
* Neutral sentiment remains the most challenging class due to overlapping contextual cues.

---

## Technologies Used

* Python
* PyTorch
* Hugging Face Transformers
* XLM-RoBERTa
* Scikit-Learn
* Pandas
* NumPy
* Matplotlib

---

## Future Work

* LoRA-based parameter-efficient fine-tuning
* Explainable AI (XAI) for model interpretation
* Support for additional low-resource languages
* Model distillation for lightweight deployment
* Real-world multilingual sentiment monitoring applications

---

## Conclusion

This project demonstrates how multilingual transformer models can learn language-independent sentiment representations and transfer that knowledge to completely unseen languages. The results highlight the effectiveness of XLM-RoBERTa for multilingual and cross-lingual sentiment analysis tasks.
