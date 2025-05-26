# Sentiment Analysis Project

## 🌐 Overview
This project is part of the **Fundamental Deep Learning course** and focuses on building a **Sentiment Analysis** system using machine learning and deep learning techniques. The goal is to classify text data into sentiment categories such as **positive, neutral, and negative**. The dataset used was collected through web scraping and includes user-generated content from public platforms.

---

## 📊 Project Objectives
- Perform end-to-end sentiment classification using Python.
- Apply feature extraction and data labeling techniques.
- Experiment with multiple training schemes using different algorithms and preprocessing methods.
- Achieve a **minimum testing accuracy of 85%**, with at least one model surpassing **92%**.

---

## 📒 Dataset
- Collected manually via **web scraping** using Python libraries such as `requests`, `BeautifulSoup`, and `selenium`.
- Sources include: e-commerce product reviews, social media comments (X/Instagram), and PlayStore app feedback.
- **Total samples collected:** ~10,000 (ensuring robust training and evaluation).
- The dataset includes **3 sentiment classes**: positive (2), neutral (1), and negative (0).

---

## ⚖️ Data Preprocessing & Feature Engineering
- Text cleaning: lowercasing, punctuation removal, stopwords filtering
- Tokenization
- Label assignment (manual + rule-based classification)
- Feature extraction using:
  - **TF-IDF**
  - **Word2Vec**
  - **Embedding layers** (for deep learning models)

---

## 🎓 Model Training & Experiments
We conducted **three training schemes** using different ML and DL models to evaluate performance:

### ✅ Training Scheme 1 – SVM
- **Model**: Support Vector Machine (SVM)
- **Feature Extraction**: TF-IDF
- **Data Split**: 80% train / 20% test
- **Accuracy**: `91.0%`
- **Performance**: Excellent on positive class (f1: 0.95); low on negative due to class imbalance

### ✅ Training Scheme 2 – Random Forest
- **Model**: Random Forest Classifier
- **Feature Extraction**: Word2Vec
- **Data Split**: 80% train / 20% test
- **Accuracy**: `87.4%`
- **Performance**: Strong recall on neutral class, but did not detect negative class (label 0)

### ✅ Training Scheme 3 – XGBoost
- **Model**: XGBoost Classifier
- **Feature Extraction**: TF-IDF
- **Data Split**: 80% train / 20% test
- **Accuracy**: `92.4%`
- **Performance**: Best overall, with balanced results across neutral and positive classes, though still weak on rare negative class

> All models output categorical sentiment: **"positive"**, **"neutral"**, **"negative"**.

---

## 🔢 Inference & Testing
- Inference is performed within the notebook file (`sentiment_analysis.ipynb`).
- Models output predictions in real-time from user input or test data.
- Screenshots and logs of inference are included as proof of implementation.

---

## 📊 Evaluation Highlights
- **Best model:** XGBoost (accuracy: 92.4%, weighted F1: 0.93)
- **Common challenge:** Very low representation of negative class (support = 16) → results in poor recall & precision for that class.
- Suggestions:
  - Apply oversampling (SMOTE) or adjust class weights
  - Add more samples for underrepresented classes

---

## 🔹 How to Run
1. Clone the repository
```bash
git clone https://github.com/yourusername/sentiment_analysis_project.git
cd sentiment_analysis_project
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Run the notebook
```bash
jupyter notebook sentiment_analysis.ipynb
```

---

## 👨‍💼 Author
- Daniel Siahaan
- Fundamental Deep Learning Course – 2025

---

## 📅 Status
✅ Completed & Submitted

> This project meets all required criteria and showcases a comprehensive approach to multi-class sentiment classification using ML and DL techniques.

---

Feel free to fork, contribute, or reach out for collaboration 🚀
