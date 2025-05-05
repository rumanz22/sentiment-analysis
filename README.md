# sentiment-analysis
Project Title: Sentiment Analysis of Tweets Using VADER
📌 Description:
This project performs sentiment analysis on a dataset of tweets collected around the 2017 Kenyan elections. The analysis classifies tweets as positive, negative, or neutral using VADER (Valence Aware Dictionary and sEntiment Reasoner) — a lexicon and rule-based sentiment analysis tool specifically attuned to sentiments expressed in social media.

🔧 Workflow Summary:
1. Data Loading and Exploration
Loaded a CSV dataset (Wote12024NLP.csv) containing raw tweets.

Tweets were embedded in a semicolon-separated string with metadata; the actual content was extracted using string operations.

2. Text Preprocessing
Cleaned tweets by:

Removing URLs, mentions, hashtags, and special characters using regular expressions.

Lowercasing text.

Tokenizing text using NLTK’s word_tokenize.

3. Sentiment Analysis with VADER
Used nltk.sentiment.SentimentIntensityAnalyzer to assign a compound score to each tweet.

Classified each tweet into:

Positive (compound ≥ 0.05)

Negative (compound ≤ -0.05)

Neutral (otherwise)

4. Insights and Observations
Sentiment Distribution:

Neutral: ~99.91%

Negative: ~0.06%

Positive: ~0.03%

This heavy skew toward neutrality suggests either a naturally neutral tone in the dataset or limitations in VADER’s sensitivity to regional or contextual sentiment.

5. Interpretation and Recommendations
Possible causes of skew:

Factual tweet content.

Overly conservative sentiment thresholds.

Language-specific subtleties not captured by VADER (which is trained on English, mostly Western corpora).

Suggestions:

Explore model fine-tuning or alternate approaches (e.g., transformer-based models).

Rebalance the dataset or use class weights to enhance model learning.

Use precision, recall, and F1-score instead of just accuracy for evaluation.

🛠️ Skills and Tools Demonstrated:
Category	Tools / Skills
Programming	Python
Data Handling	Pandas
Text Processing	Regular Expressions, NLTK (tokenization, stopwords)
Sentiment Analysis	VADER (NLTK)
NLP Preprocessing	URL/hashtag removal, lowercasing, tokenization
Analysis & Interpretation	Distribution insight, model evaluation critique
Visualization (implied)	Could be added for better sentiment representation

✅ Possible Enhancements:
Add visualizations (pie/bar charts of sentiment distribution).

Compare VADER with another method (e.g., TextBlob, BERT-based sentiment classifiers).

Include a confusion matrix and F1-scores for deeper performance evaluation.
