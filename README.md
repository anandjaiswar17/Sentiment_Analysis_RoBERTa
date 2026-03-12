# Employee Sentiment Analysis

## Project Overview

This project analyzes internal employee email communication to evaluate sentiment trends, employee engagement, and potential flight risk indicators. The analysis is performed using LLM and machine learning techniques.

The goal is to automatically label email sentiment, analyze communication patterns, identify employees with extreme sentiment trends, and detect potential flight risk employees based on negative email activity.

---

## Dataset

The dataset contains employee email records with the following attributes:

| Column | Description |
|------|-------------|
| Subject | Email subject line |
| body | Email content |
| date | Timestamp of the email |
| from | Sender email address |

From the sender email, an **employee identifier** was extracted for analysis.

---

## Project Objectives

The project performs the following tasks:

1. Sentiment labeling of employee emails
2. Exploratory Data Analysis (EDA)
3. Monthly sentiment score calculation
4. Employee ranking based on sentiment
5. Flight risk detection
6. Predictive modeling of sentiment trends

---

## Methodology

### 1. Data Cleaning
- Removed duplicate records
- Handled missing values
- Cleaned email body text using regex
- Converted date fields to datetime format

### 2. Feature Engineering
Additional features were created:
- `employee_name` extracted from sender email
- `message` combining subject and email body
- `month` extracted from date
- `message_length` for analysis

### 3. Sentiment Labeling
Sentiment analysis was performed using the **RoBERTa-based transformer model**: