# product_review_classification_system

📊 Product Review Classification System
An end-to-end Natural Language Processing (NLP) web application designed to classify customer product reviews into three distinct sentiment categories: Positive, Neutral, and Negative.
This project is built using a collaborative 3-member pipeline, integrating data preprocessing, TF-IDF machine learning modeling, and an interactive Streamlit dashboard.
👥 Team Responsibilities & Architecture
Member 1 — Dataset & NLP Preprocessing
Responsibilities: Data exploration, handling missing/duplicate values, text cleaning, tokenization, lowercasing, stopword removal, lemmatization, and sentiment label mapping.
Deliverables: preprocessing.py, cleaned dataset (preprocessed_reviews.csv).
Member 2 — Machine Learning & Model Evaluation
Responsibilities: Converting review text into numerical features using TF-IDF, training a Logistic Regression classifier, data splitting, evaluation metrics (Accuracy, Precision, Recall, F1-Score), and confusion matrix generation.
Deliverables: train_model.py, trained model (model.pkl), vectorizer (vectorizer.pkl).
Member 3 — Web App, Dashboard & Integration
Responsibilities: Building the user interface using Streamlit, integrating the trained model and vectorizer, displaying sentiment predictions, creating analytics dashboards and charts, and running live demos.
Deliverables: app.py, live dashboard application.
📂 Project Directory Structure
product_review_classification/
│
├── amazon_fine_food_review/         # Raw dataset directory
│   ├── Reviews.csv                  # Original Amazon fine food reviews
│   ├── database.sqlite              # SQLite database version
│   └── hashes.txt                   # Checksums
│
├── data/                            # Processed data directory
│   └── preprocessed_reviews.csv     # Cleaned dataset output (Member 1)
│
├── preprocessing.py                 # Text cleaning and preprocessing script
├── train_model.py                   # Model training and evaluation script (Member 2)
├── model.pkl                        # Serialized Logistic Regression model
├── vectorizer.pkl                   # Serialized TF-IDF vectorizer
├── app.py                           # Streamlit web application dashboard (Member 3)
└── README.md                        # Project documentation

🚀 Getting Started & Installation
1. Clone or Open the Repository
Clone the repository or open your workspace in GitHub Codespaces / VS Code.
2. Install Dependencies
Make sure you have Python installed, then install the required packages using pip:
pip install pandas numpy scikit-learn nltk streamlit matplotlib seaborn

3. Run Member 1: Preprocessing
Run the preprocessing script to clean the raw Amazon reviews and generate the processed dataset:
python preprocessing.py


Dataset Information
Source: Kaggle https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews?resource=download
Target Mapping:
1–2 Stars \rightarrow Negative
3 Stars \rightarrow Neutral
4–5 Stars \rightarrow Positive
