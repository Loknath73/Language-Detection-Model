🌐 AI-Powered Language Detector
An end-to-end Machine Learning project that detects the language of any given text input. The model is trained on a multi-lingual dataset supporting 23 different languages, with special optimizations implemented for South Asian languages like Bengali using advanced text tokenization techniques.

Features
Multi-language Support: Detects 23 global languages (including English, Bengali, Hindi, Spanish, French, Arabic, and more).

Balanced Dataset Optimization: Addressed data imbalance issues by oversampling minority classes (like Bengali) to ensure unbiased predictions.

Unicode-Friendly Tokenization: Built using a custom token pattern (r"[^\s]+") to prevent complex scripts (like Bengali vowels/car-signs) from breaking during vectorization.

Interactive UI: Includes a beautiful web application built with Streamlit for real-time testing.

Public Tunneling: Integrated with Localtunnel for easy cloud deployment and sharing straight from Google Colab.

Tech Stack & Libraries
Language: Python

Machine Learning: Scikit-learn (MultinomialNB, CountVectorizer)

Data Manipulation: Pandas, NumPy

Visualization: Matplotlib, Seaborn (ConfusionMatrixDisplay)

Model Deployment: Streamlit, Localtunnel

Model Persistence: Joblib

How the Model Works
Data Preprocessing: Cleaned the text by removing special characters, punctuation, and numbers using Regular Expressions (re), followed by lowercasing the text.

Text Vectorization: Converted text data into numerical vectors using CountVectorizer with a whitespace-based token pattern to preserve non-ASCII characters.

Model Training: Utilized the Multinomial Naive Bayes (NB) algorithm, which is highly efficient and standard for text classification tasks.

Evaluation: Evaluated model performance using an Accuracy Score and visualized the misclassifications using a Confusion Matrix.

 Getting Started
1. Prerequisites
Install the required Python packages:

Bash
pip install pandas scikit-learn joblib streamlit
2. Training the Model
Run the python script or Colab notebook cells to process the dataset and train the model. This will generate two serialized files:

language_detector_model.pkl (The trained Naive Bayes classifier)

vectorizer.pkl (The custom vocabulary vectorizer)

3. Running the Streamlit App
Launch the interactive web UI locally or through the tunnel:

Bash
streamlit run app.py
📈 Results & Performance
The model achieves high accuracy across all supported classes. By preserving Unicode characters, it perfectly distinguishes visually unique or low-resource scripts (like Bengali or Hindi) from European languages without falling back to major classes like English or Swedish.

Note: If you are running this project inside Google Colab, make sure to execute the Localtunnel cell to generate a public URL for accessing the Streamlit dashboard externally.
