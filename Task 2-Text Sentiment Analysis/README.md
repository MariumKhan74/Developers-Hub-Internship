# Sentiment Analysis Project

## Project Overview
This project performs sentiment analysis on text reviews using Natural Language Processing (NLP) and Machine Learning. The dataset consists of reviews labeled as positive or negative. The model is trained to classify sentiment using Logistic Regression.

## Steps
1. **Text Preprocessing**
   - Convert text to lowercase
   - Remove punctuation
   - Tokenize text into words
   - Remove stopwords
   - Perform lemmatization

2. **Feature Engineering**
   - Convert text into numerical format using TF-IDF vectorization

3. **Model Training**
   - Split data into training and testing sets
   - Train a Logistic Regression classifier

4. **Model Evaluation**
   - Evaluate the model using accuracy, precision, recall, and F1-score

5. **Prediction**
   - Implement a function to predict sentiment from new input text

## How to Run the Scripts
1. Install dependencies:
   ```bash
   pip install nltk pandas numpy scikit-learn
   ```
2. Download necessary NLTK datasets:
   ```python
   import nltk
   nltk.download('punkt')
   nltk.download('stopwords')
   nltk.download('wordnet')
   ```
3. Place your dataset (`IMDB Dataset.csv`) in the project directory, ensuring it contains `review` and `sentiment` columns.
4. Run the Python script:
   ```bash
   python sentiment_analysis.py
   ```

## Observations
- The model performs well on structured text reviews but may struggle with ambiguous or sarcastic content.
- TF-IDF captures important words but does not consider word meanings like word embeddings.
- Logistic Regression provides a baseline model; other models (e.g., Naive Bayes, Neural Networks) could be explored for improvement.

## Example Usage
To predict the sentiment of a new text, call:
```python
print(predict_sentiment("This movie was amazing, I loved it!"))
```

Expected output:
```
Positive
```

