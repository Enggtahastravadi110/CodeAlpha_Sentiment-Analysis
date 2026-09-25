# CodeAlpha Data Analytics Internship — Task 4: Sentiment Analysis

## 📌 Overview
This project analyzes customer sentiment in the **Amazon Fine Food Reviews** dataset using **VADER**, a lexicon-based NLP sentiment scoring tool. The goal is to classify reviews as Positive, Negative, or Neutral, validate that classification against real star ratings, and surface the specific words and themes driving customer satisfaction and complaints.

This task was completed as part of the **CodeAlpha Data Analytics Internship**.

## 📊 Dataset
- **Source:** [Amazon Fine Food Reviews (Kaggle)](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews)
- **Size:** 568,454 reviews (analysis run on a random 10,000-review sample for performance)
- **Fields used:** `Text` (review body), `Score` (1–5 star rating), `Time` (review timestamp)

## 🛠 Tools & Libraries
- Python, Pandas, NumPy
- NLTK (VADER SentimentIntensityAnalyzer, stopwords)
- Matplotlib, Seaborn
- WordCloud

## 🔍 Process
1. **Data cleaning** — checked for nulls and duplicates, removed duplicate reviews
2. **Sentiment scoring** — applied VADER to each review to generate a compound sentiment score (-1 to +1)
3. **Classification** — labeled each review Positive / Negative / Neutral based on the compound score
4. **Validation** — compared sentiment scores against actual star ratings to confirm accuracy
5. **Text analysis** — generated word clouds and word-frequency counts for positive vs. negative reviews
6. **Trend analysis** — examined average sentiment over time

## 📈 Key Findings
- **Sentiment split:** 87.5% Positive, 10.2% Negative, 2.3% Neutral
- **Validation:** median VADER compound score rises steadily from ~0.07 (1-star reviews) to ~0.90 (5-star reviews), confirming the sentiment scoring closely tracks real customer satisfaction
- **Rating/text mismatches:** a small subset of 4–5 star reviews contain strongly negative text — likely sarcasm or complaints unrelated to the product itself (e.g. shipping issues)
- **Positive drivers:** *(add your top words/themes from the word cloud here)*
- **Negative drivers:** *(add your top words/themes from the word cloud here)*
- **Business recommendation:** *(add your one-line recommendation here)*

## 📷 Visuals

<img width="566" height="399" alt="Screenshot 2026-09-25 195929" src="https://github.com/user-attachments/assets/4007fccd-b99e-4a72-9cfb-e62c4db579e8" />

<img width="647" height="402" alt="Screenshot 2026-09-25 200023" src="https://github.com/user-attachments/assets/1ba63b51-c9ea-41b9-8a0c-f9cde06fd142" />

<img width="804" height="304" alt="Screenshot 2026-09-25 201832" src="https://github.com/user-attachments/assets/53bbe9f7-9b3f-4faa-ace3-dfb9aad32d99" />

## ⚠️ Limitations
- VADER is a rule-based lexicon, not a trained ML model — it can misread sarcasm or complex negation
- Analysis run on a 10,000-review sample rather than the full 568K dataset for speed

## 🚀 How to Run
1. Download `Reviews.csv` from the Kaggle link above and place it in this folder
2. Install dependencies:
   ```
   pip install pandas numpy matplotlib seaborn nltk wordcloud
   ```
3. Open `Codealpha_Task4_Polished.ipynb` in Jupyter and run all cells in order

## 🎓 Internship
This project was completed as **Task 4** of the CodeAlpha Data Analytics Internship.
🔗 [CodeAlpha](https://www.codealpha.tech)
