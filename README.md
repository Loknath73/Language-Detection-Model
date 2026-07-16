# 🌍 AI-Powered Language Detector

An end-to-end Machine Learning project that automatically detects the language of a given text input. The model is trained on a multilingual dataset supporting **23 different languages**, including **English, Bengali, Hindi, Arabic, French, Spanish**, and more. To improve performance on underrepresented languages like **Bengali**, the dataset was balanced using oversampling, and Unicode-friendly tokenization was applied for accurate text processing.

---

## 🚀 Tech Stack

* **Programming Language:** Python
* **Machine Learning:** Scikit-learn
* **Algorithm:** Multinomial Naive Bayes
* **Text Vectorization:** CountVectorizer
* **Data Processing:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Model Deployment:** Streamlit
* **Model Persistence:** Joblib

---

## 📊 Dataset & Train-Test Split

| Item                | Details                                     |
| ------------------- | ------------------------------------------- |
| Dataset             | Multilingual Language Dataset               |
| Supported Languages | 23                                          |
| Train-Test Split    | **80% Training / 20% Testing**              |
| Vectorization       | CountVectorizer (`token_pattern=r"[^\s]+"`) |
| Classifier          | Multinomial Naive Bayes                     |

---

## 📈 Results

* ✅ High accuracy for multilingual language detection.
* ✅ Improved prediction for Bengali and other Unicode-based languages.
* ✅ Balanced dataset reduces bias toward majority language classes.
* ✅ Fast and lightweight model suitable for real-time prediction.

---

## ▶️ Installation

Install the required dependencies:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn streamlit joblib
```

---

## ▶️ Run the Application

Start the Streamlit application:

```bash
streamlit run app.py
```

If you are using **Google Colab**, you can expose the Streamlit app publicly using **Localtunnel**.

---

## 📂 Generated Files

After training the model, the following files will be created:

* `language_detector_model.pkl`
* `vectorizer.pkl`

---

## 👨‍💻 Author

**Loknath Basak Anup**
B.Sc. in Computer Science & Engineering
United International University (UIU)

---

⭐ If you found this project useful, consider giving it a **Star** on GitHub.
