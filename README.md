# 🇺🇸 Trump vs Biden Tweet Sentiment Analysis

This project performs sentiment analysis on tweets related to **Donald Trump** and **Joe Biden** using Natural Language Processing (NLP) and a machine learning classifier. It includes full data cleaning, feature engineering, visualizations, and a logistic regression model to predict whether a tweet expresses **Positive**, **Negative**, or **Neutral** sentiment.

---

## 🧠 Project Objective

To analyze public sentiment from Twitter data about U.S. political figures and build a machine learning model that classifies sentiment based on tweet content.

---

## 📁 Dataset

Used two CSV files collected from Twitter:
- `hashtag_donaldtrump.csv`
- `hashtag_joebiden.csv`

### Common Columns Used:
- `tweet`: The main text content of the tweet  
- `likes`, `retweet_count`: Used for exploratory analysis  
- `Candidate`: Label manually added to distinguish Trump and Biden tweets  

---

## 🧹 Data Preprocessing

- Removed unnecessary columns (`user_id`, `location`, etc.)
- Dropped rows with missing tweets
- Combined the two datasets and added a `Candidate` column
- Cleaned the tweet text:
  - Converted to lowercase
  - Removed URLs, mentions, hashtags, emojis, and special characters
  - Stored in a new column: `clean_tweet`

---

## 📊 Exploratory Data Analysis

📌 *Visualizations like pie charts, bar graphs, and word clouds were created to understand the sentiment distribution across both candidates.*

### 📍 Sentiment Distribution for Trump Tweets
![Screenshot 2025-06-18 201554](https://github.com/user-attachments/assets/b86b4924-7a82-4223-87ae-9635a8f3bdf0)


### 📍 Sentiment Distribution for Biden Tweets
![Screenshot 2025-06-18 201643](https://github.com/user-attachments/assets/fa53efb1-d05b-4c1c-81e0-8e63a83913a7)


### 📍 Overall Comparison of Sentiments
![Screenshot 2025-06-18 200848](https://github.com/user-attachments/assets/fdad664a-2de5-4e3e-a39a-a6a173189c1b)

---

## 🤖 Model Building

### Features:
- `clean_tweet` (vectorized using CountVectorizer)
- `Candidate` (encoded using OneHotEncoder)

### Model:
- **Logistic Regression**

### Accuracy:
- Achieved an accuracy of **95.86%** on the test set

---

## 🧪 Sample Results

| Tweet Text                            | Candidate | Predicted Sentiment |
|--------------------------------------|-----------|----------------------|
| "I love what Trump said today"       | Trump     | Positive             |
| "Biden’s policies are not working"   | Biden     | Negative             |

---

## 🛠️ Tools & Libraries

- Python 🐍
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 📌 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/divyanshdahikar/Trump-Biden-Sentiment-Analysis
