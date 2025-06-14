# 🇺🇸 Trump vs Biden Tweet Sentiment Analysis

This project analyzes public sentiment from tweets related to Donald Trump and Joe Biden during the U.S. political climate. It includes full data cleaning, preprocessing, visualizations, and a machine learning model to classify sentiments as **Positive**, **Negative**, or **Neutral**.

---

## 🧠 Project Objective

To build a machine learning model that can accurately predict the sentiment of tweets related to Donald Trump and Joe Biden using Natural Language Processing (NLP) techniques.

---

## 📁 Dataset

Two separate CSV files were used:
- `hashtag_donaldtrump.csv`
- `hashtag_joebiden.csv`

Each file contains tweet-related metadata such as:
- `tweet`: The actual tweet text  
- `likes`, `retweet_count`: Engagement features  
- `created_at`, `user_name`, `user_location`, etc.

### Data Cleaning Highlights:
- Removed unnecessary or null columns (e.g., user ID, coordinates)
- Removed rows with missing tweet text
- Combined both datasets with a new column `Candidate` (Trump or Biden)

---

## 🧹 Text Preprocessing

Each tweet was cleaned using the following steps:
- Lowercased
- Removed URLs using regex: `r"http\S+"`
- Removed mentions, hashtags, special characters
- Removed extra whitespaces

Cleaned tweets were stored in a new column: `clean_tweet`

---

## 📊 Exploratory Data Analysis

Visualized insights like:
- Sentiment distribution using pie charts
- Trump vs Biden sentiment comparison with bar plots
- Example tweets per sentiment per candidate

---

## 🤖 Model Building

### Features:
- `clean_tweet` (text data)
- `Candidate` (Trump or Biden)

### Preprocessing:
- CountVectorizer for tweet text
- OneHotEncoder for candidate

### Classifier:
- **Logistic Regression**

### Performance:
- **Accuracy: 95.86%**

---

## 🔍 Sample Results

| Tweet                                | Candidate | Predicted Sentiment |
|-------------------------------------|-----------|----------------------|
| "I love what Trump said today"      | Trump     | Positive             |
| "Biden’s policies are not helping"  | Biden     | Negative             |

---

## 📦 Tech Stack

- Python 🐍
- Pandas & NumPy
- Scikit-learn
- Seaborn & Matplotlib
- Jupyter Notebook
- TextBlob
- vaderSentiment

---

## 📌 How to Run

1. Clone the repository
2. Install dependencies  
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
