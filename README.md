# Sentiment Analysis and User Review Insights for Large Language Model Applications

## Overview

This repository contains the documentation, experiments, and analysis for a study on **sentiment classification and user review insights of Large Language Model (LLM) applications** such as GPT, Gemini, Claude, Perplexity, Grok, and DeepSeek.

The project focuses on three main objectives:

1. Building an accurate sentiment classification model for imbalanced review data.
2. Extracting meaningful insights from negative user reviews.
3. Analyzing sentiment shifts across application versions.

---

## Repository Contents

This repository includes the following files and folders:

### Dataset
- **pekan-raya-statistika.zip**  
  Contains the dataset provided for the competition/research.  
  Includes training and testing data with review-related attributes such as:
  - Comment
  - Timestamp
  - AppVersion
  - Sentiment (training only)

### Experiments
- **Model Building Experiment**  
  Contains model comparison experiments using multiple encoders and classifiers.

### Prediction
- **Inference Prediction**  
  Contains final inference results on test data.

### Analysis
- **User Review Analysis**  
  Contains exploratory analysis, negative review insights, topic modeling, and version-based sentiment analysis.

---

## Methodology

### 1. Text Preprocessing
Several preprocessing steps were applied:

- Translation of non-English reviews into English
- Lowercasing
- Emoji conversion to text
- Unicode normalization
- Repeated character normalization
- Duplicate removal

### 2. Feature Extraction

Pretrained transformer encoders were used to convert reviews into embeddings, including:

- Multilingual E5
- Qwen3 Embedding
- twitter-RoBERTa sentiment model
- Other HuggingFace encoders

### 3. Classification Models

The embeddings were used as input for:

- XGBoost
- LightGBM
- CatBoost
- Artificial Neural Network

### 4. Evaluation Metric

Primary metric:

- **Macro F1 Score**

Chosen due to class imbalance in sentiment labels.

### 5. User Review Analysis

Includes:

- Frequent complaint keywords
- Topic Modeling (BERTopic)
- Cross-version sentiment comparison
- Chi-Square statistical testing

---

## Key Findings

### Best Sentiment Model

Top-performing combinations achieved **Macro F1 = 0.66–0.67**, with:

- Multilingual E5
- twitter-RoBERTa-stm

### Main Negative Review Themes

Common complaints include:

- Reliability issues
- Slow responses
- Poor feature performance
- Login / verification problems
- Subscription cost dissatisfaction

### Version-Based Insights

Some applications showed significant sentiment shifts across versions, indicating that certain updates improved or worsened user experience.

---

## Practical Implications

Developers of LLM applications can use this framework to:

- Monitor user sentiment continuously
- Detect problematic releases early
- Prioritize fixes based on recurring complaints
- Benchmark against competitors

---

## Tools & Libraries

Used in this project:

- Python
- Pandas
- Scikit-learn
- XGBoost
- LightGBM
- CatBoost
- PyTorch
- HuggingFace Transformers
- BERTopic
- Matplotlib / Seaborn

---

## How to Use

1. Download dataset from `pekan-raya-statistika.zip`
2. Run notebooks/scripts in:
   - `Model Building Experiment`
   - `Inference Prediction`
   - `User Review Analysis`

---

## License

For academic and research purposes only.
