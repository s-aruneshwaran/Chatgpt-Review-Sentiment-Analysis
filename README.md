# ChatGPT Review Sentiment Analysis

## Project Overview
This project analyzes user reviews of ChatGPT to understand customer sentiment, common feedback patterns, and overall product perception using Natural Language Processing (NLP) techniques.

The analysis extracts insights from textual reviews and ratings to identify user satisfaction, common issues reported by users, and features that customers appreciate the most.

---

## Objectives
- Perform sentiment analysis on user reviews
- Identify common phrases in positive and negative feedback
- Detect major issues reported by users
- Analyze sentiment trends over time
- Estimate customer loyalty using Net Promoter Score (NPS)

---

## Dataset
The dataset contains user reviews of ChatGPT with the following fields:

- **Review ID**
- **Review Text**
- **Ratings (1–5 stars)**
- **Review Date**

---

## Technologies Used
- Python
- Pandas
- Plotly
- Scikit-learn
- TextBlob (for sentiment analysis)

---

## Methodology

### 1. Data Cleaning
- Checked for missing values in the dataset
- Replaced missing review text with empty strings

### 2. Sentiment Analysis
- Applied polarity-based sentiment classification using **TextBlob**
- Classified reviews into:
  - Positive
  - Neutral
  - Negative

### 3. Phrase Extraction
- Used **CountVectorizer** to extract frequent bigrams and trigrams
- Identified common phrases in positive and negative reviews

### 4. User Problem Analysis
Grouped negative phrases into broader problem categories such as:

- Incorrect answers
- App performance issues
- User interface problems
- Missing or broken features
- Poor response quality

### 5. Sentiment Trends Over Time
- Converted review dates into time-series format
- Analyzed how sentiment changed over time

### 6. Net Promoter Score (NPS)
Customer loyalty was estimated using ratings:

- **Promoters:** 5-star ratings  
- **Passives:** 4-star ratings  
- **Detractors:** 3 stars and below  

NPS was calculated using:

NPS = %Promoters − %Detractors

---

## Key Insights

- The majority of reviews are **positive**, indicating strong user satisfaction.
- Frequent positive phrases highlight the **usefulness and accuracy of the tool**.
- Common negative feedback includes:
  - incorrect answers
  - performance issues
  - missing features
- Sentiment trends show consistent user engagement over time.
- The calculated **Net Promoter Score (NPS) ≈ 64**, which indicates **excellent customer loyalty**.

---

## Visualizations

The project includes several visualizations:

- Sentiment distribution of reviews
- Most common positive phrases
- Most common negative phrases
- Major user problem categories
- Sentiment trends over time

---

## Repository Structure

```
chatgpt-review-sentiment-analysis
│
├── data
│   └── chatgpt_reviews.csv
│
├── notebooks
│   └── chatgpt_review_analysis.ipynb
│
├── images
│   ├── sentiment_distribution.png
│   ├── positive_phrases.png
│   ├── negative_phrases.png
│   ├── user_problems.png
│   └── sentiment_trends.png
│
├── requirements.txt
└── README.md
```

---

## Future Improvements

Possible extensions for this project include:

- Using transformer-based models such as **BERT** for improved sentiment analysis
- Applying **topic modeling** to discover deeper themes in reviews
- Building an **interactive dashboard** for real-time review monitoring
- Deploying the analysis pipeline as a **web application**
