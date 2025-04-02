Fake News Detection

Overview

This project is an AI-powered model designed to classify news articles as either real or fake. It uses Natural Language Processing (NLP) techniques combined with deep learning methods to analyze and detect misinformation in news content.

Features

Uses NLP techniques like tokenization, lemmatization, and stopword removal

Employs a Bidirectional LSTM model for classification

Visualizes word distributions and word clouds for real vs. fake news

Implements TensorFlow and Keras for model training and evaluation

Achieves high accuracy in detecting fake news

Saves the trained model for future predictions

Installation

To run this project, you need to install the required dependencies. You can do this by running the following commands:

pip install --upgrade tensorflow-gpu==2.18
pip uninstall -y tensorflow
pip install --upgrade tensorflow
pip install plotly
pip install nbformat
pip install nltk
pip install spacy
pip install WordCloud
pip install gensim
pip install seaborn
pip install scikit-learn

Dataset

The dataset used consists of two CSV files:

True.csv: Contains real news articles

Fake.csv: Contains fake news articles

The dataset is preprocessed by removing stopwords and punctuation, then tokenized for input into the LSTM model.

Usage

1. Load the dataset

import pandas as pd

# Load the data
true_df = pd.read_csv("True.csv")
fake_df = pd.read_csv("Fake.csv")

2. Preprocess the text

import nltk
from nltk.corpus import stopwords
nltk.download("stopwords")

stop_words = stopwords.words('english')

3. Train the model

from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense, Embedding, LSTM, Bidirectional

model = Sequential()
model.add(Embedding(input_dim=10000, output_dim=128))
model.add(Bidirectional(LSTM(128)))
model.add(Dense(128, activation='relu'))
model.add(Dense(1, activation='sigmoid'))
model.compile(optimizer='adam', loss='binary_crossentropy', metrics=['accuracy'])

4. Evaluate the model

from sklearn.metrics import accuracy_score
accuracy = accuracy_score(y_test, predictions)
print(f'Model Accuracy: {accuracy}')

Model Saving and Deployment

The trained model can be saved and used for future predictions.

model.save("fake_news_model.keras")

To reload the model:

from tensorflow.keras.models import load_model
model = load_model("fake_news_model.keras")

Google Colab Notebook

You can access the project on Google Colab using the following link:Fake News Detection - Colab Notebook

Contributing

Feel free to fork this repository and submit pull requests for improvements.

License

This project is licensed under the MIT License.


