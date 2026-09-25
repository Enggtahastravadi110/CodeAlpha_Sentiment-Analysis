CodeAlpha Data Analytics Internship — Task 4: Sentiment Analysis
📌 Overview

This project analyzes customer sentiment in the Amazon Fine Food Reviews dataset using VADER, a lexicon-based NLP sentiment scoring tool. The goal is to classify reviews as Positive, Negative, or Neutral, validate that classification against real star ratings, and surface the specific words and themes driving customer satisfaction and complaints.

This task was completed as part of the CodeAlpha Data Analytics Internship.

📊 Dataset
Source: Amazon Fine Food Reviews (Kaggle)
Size: 568,454 reviews (analysis run on a random 10,000-review sample for performance)
Fields used: Text (review body), Score (1–5 star rating), Time (review timestamp)
🛠 Tools & Libraries
Python, Pandas, NumPy
NLTK (VADER SentimentIntensityAnalyzer, stopwords)
Matplotlib, Seaborn
WordCloud
🔍 Process
Data cleaning — checked for nulls and duplicates, removed duplicate reviews
Sentiment scoring — applied VADER to each review to generate a compound sentiment score (-1 to +1)
Classification — labeled each review Positive / Negative / Neutral based on the compound score
Validation — compared sentiment scores against actual star ratings to confirm accuracy
Text analysis — generated word clouds and word-frequency counts for positive vs. negative reviews
Trend analysis — examined average sentiment over time
📈 Key Findings
Sentiment split: 87.5% Positive, 10.2% Negative, 2.3% Neutral
Validation: median VADER compound score rises steadily from ~0.07 (1-star reviews) to ~0.90 (5-star reviews), confirming the sentiment scoring closely tracks real customer satisfaction
Rating/text mismatches: a small subset of 4–5 star reviews contain strongly negative text — likely sarcasm or complaints unrelated to the product itself (e.g. shipping issues)
Positive drivers: (add your top words/themes from the word cloud here)
Negative drivers: (add your top words/themes from the word cloud here)
Business recommendation: (add your one-line recommendation here)
📷 Visuals

(Add screenshots here after running the notebook — recommended: sentiment distribution chart, rating validation boxplot, and both word clouds)

![Sentiment Distribution](images/sentiment_distribution.png)
![Rating Validation](images/rating_validation.png)
![Word Clouds](images/wordclouds.png)
⚠️ Limitations
VADER is a rule-based lexicon, not a trained ML model — it can misread sarcasm or complex negation
Analysis run on a 10,000-review sample rather than the full 568K dataset for speed
🚀 How to Run
Download Reviews.csv from the Kaggle link above and place it in this folder
Install dependencies:
   pip install pandas numpy matplotlib seaborn nltk wordcloud
Open Codealpha_Task4_Polished.ipynb in Jupyter and run all cells in order
🎓 Internship

This project was completed as Task 4 of the CodeAlpha Data Analytics Internship. 🔗 CodeAlpha
