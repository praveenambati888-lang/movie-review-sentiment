# movie-review-sentiment
NLP project for analyzing and classifying movie review sentiments.
# Movie Review Sentiment Analysis

Classifies IMDB movie reviews as positive or negative (25,000 training and 25,000 test reviews, perfectly balanced).

## Results
- Baseline TF-IDF + logistic regression: 88% accuracy
- After cleaning HTML tags and adding word pairs (bigrams): 89.5% accuracy
- Most negative words: bad, worst, awful. Most positive: great, excellent, wonderful.
- Correctly handles negation such as "not good" thanks to word pairs.

## Method
1. Loaded the IMDB dataset with the Hugging Face datasets library
2. Converted text to numbers with TF-IDF (single words and word pairs)
3. Trained logistic regression and compared against the baseline
4. Inspected the strongest words per class and built a small predict function

## Limitations
Reads words, not meaning, so sarcasm and mixed reviews can fool it.

## Tools
Python, pandas, scikit-learn, Hugging Face datasets, Google Colab
