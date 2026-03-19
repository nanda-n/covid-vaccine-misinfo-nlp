# covid-vaccine-misinfo-nlp
Detecting COVID-19 vaccine misinformation on Twitter using traditional machine learning and domain-specific Transformers
Detecting COVID-19 Vaccine Misinformation on Twitter

This repository contains the research and implementation of a binary classification system designed to detect tweets that support COVID-19 vaccine misinformation. The study compares a traditional machine learning baseline against a state-of-the-art domain-specific transformer model.

📌 Project Overview

The core of this research is a comparative analysis between Logistic Regression (with TF-IDF features) and COVID-Twitter-BERT (CT-BERT). The project utilizes a subset of the COVMis-Stance dataset to evaluate how model complexity impacts performance in low-resource environments (small datasets).

Key Result

Contrary to standard deep learning expectations, the Logistic Regression model achieved superior generalization on the final test set compared to CT-BERT, which suffered from overfitting due to the limited training data (97 samples).

📊 Performance Summary

Model

Split

Accuracy

Macro F1-Score

Logistic Regression

Test

0.67

0.62

CT-BERT

Validation

0.86

0.85

CT-BERT

Test

0.52

0.52

🛠️ Methodology

1. Data Processing

Dataset: Filtered vaccine-related tweets from COVMis-Stance.

Labeling: Simplified original stance labels into misinfo (supporting claims) and not_misinfo (neutral or refuting).

Cleaning: Removed URLs, @mentions, hashtag symbols, and normalized text to lowercase.

2. Models

Baseline: Logistic Regression with TF-IDF vectorization (unigrams + bigrams, 3000 features).

Transformer: digitalepidemiologylab/covid-twitter-bert-v2 (CT-BERT), fine-tuned with a learning rate of 2e-5 and early stopping.

📂 Repository Structure

/paper: Contains the full research paper in PDF format.

/notebooks: Jupyter notebooks detailing data cleaning and model training.

requirements.txt: Necessary libraries to reproduce the environment.

📝 Conclusion

This project demonstrates that in low-resource settings, structural complexity (Transformers) does not replace the necessity of large-scale datasets. Simple statistical models can provide more resilient performance when data is scarce.

Author: Nikhil Emmanuel Nanda

Institution: Mountain House High School

License: MIT
