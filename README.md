# Spam Classification with Machine Learning

## Overview

This project focuses on building a spam classification system using various machine learning models to classify SMS messages as either **ham** or **spam**. Using the popular **SMS Spam Collection dataset** from the **UCI Machine Learning Repository**, the project implements data preprocessing techniques to clean and prepare the SMS data for modeling. 

A variety of machine learning algorithms are explored, including **Logistic Regression**, **Naive Bayes**, **SVM**, and **Decision Trees**, allowing for a comprehensive evaluation and comparison of their performance. Ultimately, the **Stacking Classifier** emerged as the best-performing model, achieving high accuracy and precision in effectively classifying SMS messages.


### Key Features:
- Preprocessing of SMS data using techniques like stopword removal, stemming, and vectorization using the TF-IDF technique.
- Multiple machine learning algorithms tested, including **Logistic Regression**, **Naive Bayes**, **SVM**, **Decision Tree**, and **Ensemble Models**.
- The final model uses a **Stacking Classifier** that combines the predictions of several base models for improved accuracy.
- **Stacking Classifier Results:**
  - **Accuracy:** 0.99
  - **Precision:** 1.0
  - **Recall:** 0.95
- Model and vectorizer are saved using **Joblib** for reuse in real-time classification.


## Dataset

The dataset used is the [SMS Spam Collection](https://archive.ics.uci.edu/ml/datasets/sms+spam+collection) from the UCI Machine Learning Repository, containing 5,572 SMS messages labeled as 'ham' or 'spam'.

## Project Structure

```
sms-spam-classifier-ml/
│
├── spam_dataset.csv
├── app.ipynb
├── stacking_model.pkl
├── tfidf_vectorizer.pkl
├── README.md
└── requirements.txt
```

## Installation

To run this project locally, follow these steps:

- Clone the repository:
```git clone https://github.com/AhmedNabil03/sms-spam-classifier-ml.git```

- Navigate to the project directory:
```cd sms-spam-classifier-ml```

- Install the required dependencies:
```pip install -r requirements.txt```


## Usage
- Classifying an SMS:
You can use the classify_sms(sms) function defined in the notebook to classify a new SMS message.

Here’s an example of how to call it:

```python
from app import classify_sms

sms = "Congratulations! You've won a $1000 gift card. Call now!"
result = classify_sms(sms)
print(result)  # Output: Spam
```
