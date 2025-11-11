# Emotion Classification Project
This project focuses on classifying emotions from textual data using various Natural Language Processing (NLP) techniques and Machine Learning models.

# Project Overview
The goal of this project is to build a model that can accurately predict the emotion conveyed in a given text snippet. The emotions considered are 'sadness', 'anger', 'love', 'surprise', 'fear', and 'joy'.

## Dataset
The project uses a dataset (assumed to be train.txt) containing text samples labeled with their corresponding emotions.

## Data Loading and Initial Exploration
The dataset is loaded into a pandas DataFrame with columns 'text' and 'emotion'.
Initial checks for null values were performed, confirming no missing data.
Unique emotions in the dataset were identified.

## Data Preprocessing
To prepare the text data for model training, the following preprocessing steps were applied:

Emotion Encoding: Categorical emotion labels were mapped to numerical values.
Lowercasing: All text was converted to lowercase to ensure consistency.
Punctuation Removal: Punctuation marks were removed from the text.
Number Removal: Numerical digits were removed from the text.
Emoji Removal: Non-ASCII characters (assumed to include emojis) were removed.
Stop Word Removal: Common English stop words (e.g., 'the', 'is', 'a') were removed to reduce noise and focus on more meaningful words.
Feature Extraction
Two primary feature extraction techniques were used to convert the preprocessed text into numerical representations:

### Bag-of-Words (BoW): Using CountVectorizer to count word occurrences.
### TF-IDF (Term Frequency-Inverse Document Frequency): Using TfidfVectorizer to weigh words based on their importance in the document and corpus.
### Model Training and Evaluation

The processed data was split into training and testing sets (80% training, 20% testing).

## Three different machine learning models were trained and evaluated:

### 1. Multinomial Naive Bayes with Bag-of-Words (BoW)
Model: MultinomialNB
Vectorizer: CountVectorizer
Accuracy: 0.768125

### 2. Multinomial Naive Bayes with TF-IDF
Model: MultinomialNB
Vectorizer: TfidfVectorizer
Accuracy: 0.7275

### 3. Logistic Regression with TF-IDF
Model: LogisticRegression
Vectorizer: TfidfVectorizer
Accuracy: 0.8628125
Results
The Logistic Regression model, when combined with TF-IDF feature extraction, achieved the highest accuracy of approximately 86.28% on the test set, making it the best-performing model among those tested for this emotion classification task.
