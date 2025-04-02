# 📰 Fake News Detection using NLP & Deep Learning

🚀 This project detects **Fake News** using **Natural Language Processing (NLP)** and **Deep Learning (BiLSTM)**. It analyzes news articles and classifies them as **Real or Fake**, helping combat misinformation.

---

## 📌 Features
✅ **NLP preprocessing** – Tokenization, stopword removal, and text cleaning  
✅ **Bidirectional LSTM model** – Captures context from both past & future words  
✅ **Trained on real & fake news datasets** – Ensures reliable classification  
✅ **Data visualization** – Uses WordCloud and Seaborn for insights  

---

## 🛠️ Technologies Used
- **Python** – Pandas, NumPy, Matplotlib, Seaborn  
- **TensorFlow / Keras** – Deep Learning Model  
- **NLP Libraries** – NLTK, spaCy, Gensim  
- **Data Visualization** – WordCloud, Seaborn, Plotly  

---

## 📂 Dataset
This model is trained on two datasets:  
- **True.csv** – Contains real news articles  
- **Fake.csv** – Contains fake news articles  
The dataset is preprocessed by removing stopwords, punctuation, and unnecessary text elements.  

---

## 🚀 Installation & Setup

1️⃣ **Clone this repository:**  
```bash
git clone https://github.com/CoderGuy009/Fake-News-Detection.git
cd Fake-News-Detection
```

2️⃣ **Install dependencies:**  
```bash
pip install -r requirements.txt
```

3️⃣ **Download necessary NLTK data:**  
```python
import nltk
nltk.download('stopwords')
nltk.download('punkt')
```

4️⃣ **Run the model training script:**  
```bash
python fake_news_detection.py
```

---

## 🎯 How It Works
1️⃣ **Data Preprocessing** – Tokenizes and removes stopwords from text  
2️⃣ **Feature Engineering** – Converts text into numerical sequences  
3️⃣ **Model Training** – Uses a **Bidirectional LSTM model** for classification  
4️⃣ **Prediction** – Determines whether news is **Fake or Real**  

---

## 🔗 Try It on Google Colab
Run this project directly in **Google Colab**:  
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/16AOwA28L8MZFVZ-pxFSk8tcsdzbFegH2?usp=drive_link)  

---

## 📌 Saving & Loading the Model
To save the trained model:  
```python
model.save("fake_news_model.keras")
```
To load the trained model:  
```python
from tensorflow.keras.models import load_model
model = load_model("fake_news_model.keras")
```

---

## 🤝 Contributing
Feel free to **fork this repo**, make improvements, and submit a **pull request**!  

---

## 📜 License
This project is open-source under the **MIT License**.  

📌 **Star this repo** ⭐ & contribute to fight fake news! 🚀
