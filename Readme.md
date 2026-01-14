# Emotion Detection from Text

A simple **machine learning project** that classifies the emotion expressed in a short text input (e.g. tweet, message, sentence) into one of six basic emotions:

- 😊 **joy**
- 😢 **sadness**
- 😡 **anger**
- 😨 **fear**
- 😲 **surprise**
- 😐 **love**

Built with **Python**, **scikit-learn**, and a **Flask** web interface.

## ✨ Features

- Web interface where you can type any text and get an instant emotion prediction
- Trained on the popular **Emotion Dataset** (multiple variants available on Kaggle/Hugging Face)
- Uses **TF-IDF vectorization** + classic ML classifiers
- Simple and fast — good for learning text classification basics

## Demo (when running locally)

http://127.0.0.1:5000/

![Emotion Detection Demo](https://via.placeholder.com/800x450.png?text=Emotion+Detection+Web+App+Screenshot)  
*(Replace this placeholder with a real screenshot of your running app)*

## 📂 Project Structure

```
Emotion/
├── app.py                  # Flask application + model loading & prediction
├── model_training.ipynb    # Jupyter notebook with data exploration, training & evaluation
├── templates/
│   └── index.html          # Main web page with input form
├── static/
│   └── style.css           # Optional custom styling
├── requirements.txt        # List of Python dependencies
├── model/                  # (generated) saved model files (optional)
│   ├── best_model.pkl
│   └── tfidf_vectorizer.pkl
└── README.md
```

## 🛠 Technologies Used

- **Python** 3.x
- **Flask** – web framework
- **scikit-learn** – TF-IDF + classifiers (Logistic Regression, SVM, Naive Bayes, etc.)
- **pandas** & **numpy** – data handling
- **joblib** – model & vectorizer serialization
- **HTML + CSS** – simple frontend

## ⚡ Quick Start (Local)

1. **Clone the repository**

   ```bash
   git clone https://github.com/rajeesing/Emotion.git
   cd Emotion
   ```

2. **(Recommended) Create virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate      # Linux / macOS
   venv\Scripts\activate         # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

   Typical content of `requirements.txt`:
   ```
   flask
   scikit-learn
   pandas
   numpy
   joblib
   ```

4. **Train the model (if you don't have saved model files yet)**

   ```bash
   jupyter notebook model_training.ipynb
   ```

   Run all cells → it should save `best_model.pkl` and `tfidf_vectorizer.pkl` in the `model/` folder.

5. **Run the web application**

   ```bash
   python app.py
   ```

6. Open your browser and go to:

   **http://127.0.0.1:5000/**

## 🔍 Model & Performance (example from training notebook)

Common results you might see (will vary depending on dataset split & model):

| Model                  | Accuracy | F1-Score (weighted) |
|------------------------|----------|----------------------|
| Logistic Regression    | ~0.88    | ~0.87                |
| Linear SVM             | ~0.87    | ~0.86                |
| Multinomial Naive Bayes| ~0.85    | ~0.84                |
| Random Forest          | ~0.82    | ~0.81                |

*Best model usually: Logistic Regression with TF-IDF*

## 📊 Dataset

Commonly used datasets for this project:

- **Emotion Dataset** (Kaggle / Hugging Face)  
  ~20,000–40,000 labeled sentences/tweets  
  6 classes: sadness, joy, love, anger, fear, surprise

## 🚀 Possible Next Steps

- Try transformer-based models (DistilBERT, BERT, RoBERTa)
- Add confidence scores / top-3 predictions
- Improve UI (Bootstrap, Tailwind, React frontend)
- Deploy to Render / Railway / Heroku / Vercel
- Add multi-language support
- Create a Chrome extension or Telegram bot

## 📄 License

MIT License – feel free to use, modify and learn from this project!

## 💬 Connect

Built by [Rajeev](https://github.com/rajeesing)  
Questions, suggestions or want to collaborate? Feel free to open an issue!

#MachineLearning #NLP #TextClassification #Python #Flask #EmotionDetection
