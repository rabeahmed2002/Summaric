# Sentiment Analysis with Text Summarization

## Overview

This project leverages **RoBERTa** for **Sentiment Analysis** and **T5** for **Text Summarization** to analyze and summarize text data effectively. The goal of this project is to demonstrate how NLP models can be combined for practical tasks such as sentiment extraction and text summarization in one pipeline.

### Key Features:
- **Sentiment Analysis**: Uses **RoBERTa** (Robustly Optimized BERT Pretraining Approach) to classify text into categories such as Positive, Negative, or Neutral.
- **Text Summarization**: Uses **T5** (Text-To-Text Transfer Transformer) to generate a concise summary of the provided text while retaining the key points.

## Setup

1. **Clone this repository** to your local machine:
    ```bash
    git clone https://github.com/your-username/sentiment-analysis-text-summarization.git
    ```

2. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the project**:
    To perform sentiment analysis and text summarization, run the script:
    ```bash
    python run_analysis.py
    ```

### Pre-trained Models Used:
- **RoBERTa**: Used for sentiment classification tasks, pretrained on a large corpus of text.
- **T5**: Used for summarization tasks, pre-trained on the large text-to-text dataset.

## Usage Example

```python
from transformers import pipeline

# Sentiment analysis
sentiment_model = pipeline("sentiment-analysis", model="roberta-large")
result = sentiment_model("I love working on NLP projects!")
print(result)

# Text summarization
summarization_model = pipeline("summarization", model="t5-base")
summary = summarization_model("Your long text here.")
print(summary)
