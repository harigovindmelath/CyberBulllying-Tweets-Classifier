# CyberBulllying-Tweets-Classifier

This project implements a machine learning-based classification model to detect and categorize cyberbullying tweets. The model leverages Natural Language Processing (NLP) techniques, including text preprocessing, sentiment analysis, and feature extraction using TF-IDF, combined with a Random Forest Classifier to classify tweets as either "Cyberbullying" or "Not Cyberbullying."
Key Features:
    Text Preprocessing: Removes URLs, mentions, hashtags, punctuation, and converts text to lowercase to standardize input for the model.
    Sentiment Analysis: Uses TextBlob to analyze the sentiment polarity of tweets, helping to identify emotional tone (positive, negative, or neutral).
    TF-IDF Vectorization: Extracts meaningful features from tweet text by calculating term frequency-inverse document frequency scores, which represent the importance of words in the dataset.
    Random Forest Classifier: A robust and versatile algorithm used to classify tweets with binary labels (cyberbullying or not).
    Custom Predict Function: Allows real-time prediction of new tweets by combining preprocessing, sentiment analysis, and classification.

Dataset

The model is trained on a synthetic cyberbullying dataset, which includes:

Text of tweets (tweet_text).
Target labels (cyberbullying_type), where tweets are categorized as either cyberbullying or not cyberbullying.

Methodology

Dataset Preparation:
    Load and clean the dataset.
    Preprocess the tweets to remove unnecessary elements (e.g., URLs, mentions, special characters).
    Perform sentiment analysis to assign a polarity score to each tweet.

Feature Engineering:
    Apply TF-IDF vectorization to convert textual data into numerical format.
    Combine sentiment polarity as an additional feature with the TF-IDF vectorized data.

Model Training:
    Split the data into training and testing sets using an 80-20 split.
    Train the Random Forest Classifier with 100 estimators and evaluate the model using a classification report (precision, recall, F1-score).
    
Prediction:
     A custom function is implemented to preprocess and predict the category of any given tweet, making it user-friendly and suitable for real-time applications.

Outputs

The model provides:

 A classification result: Cyberbullying or Not Cyberbullying.
Sentiment polarity scores for analyzed tweets.
Performance metrics (e.g., precision, recall, and F1-score) for evaluating the model’s effectiveness.


Dependencies

    pandas
    scikit-learn
    TextBlob
    re
    pickle

Usage

Clone the repository:

    git clone https://github.com/your-repo-name.git

Install dependencies:

    pip install -r requirements.txt

Run the model training script or use the prediction function:

    python classify_tweets.py
