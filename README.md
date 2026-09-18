# 📧 Email Spam Detection System using Machine Learning

## 📌 Project Overview

The **Email Spam Detection System** is a Machine Learning project that classifies text messages/emails into two categories:

* **Spam** — unwanted or promotional messages
* **Ham** — legitimate messages

The project uses **Natural Language Processing (NLP)** techniques to convert text into numerical features and a **Multinomial Naive Bayes** classifier to predict whether a message is spam or ham.

The complete implementation is developed in a Jupyter Notebook using Python and Scikit-learn.

---

## 🎯 Objectives

* Detect spam emails/messages automatically.
* Classify messages as **Spam** or **Ham**.
* Perform text preprocessing and feature extraction.
* Train a Machine Learning classification model.
* Evaluate the model using multiple performance metrics.
* Visualize commonly used words in spam messages.
* Provide a function for testing new email/message text.

---

## ✨ Features

### 📩 Spam/Ham Classification

The system classifies an input message into:

```text
Spam Email
```

or

```text
Ham Email
```

### 🔤 Text Vectorization

The project uses **CountVectorizer** to convert text messages into numerical feature vectors that can be processed by the Machine Learning model.

### 🤖 Machine Learning Model

The project uses:

**Multinomial Naive Bayes**

which is suitable for text classification problems.

### ☁️ Word Cloud

A Word Cloud is generated to visualize frequently occurring words in spam messages.

### 📊 Model Evaluation

The model is evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Confusion Matrix
* Classification Report
* ROC Curve

### 🔍 Custom Email Detection

The notebook contains a `detect_spam()` function that can be used to classify new messages.

Example:

```python
sample_email = 'Free Tickets for IPL'
result = detect_spam(sample_email)
print(result)
```

Output:

```text
This is a Spam Email!
```

---

## 🛠️ Technologies Used

| Technology / Library    | Purpose                 |
| ----------------------- | ----------------------- |
| Python                  | Programming language    |
| Pandas                  | Data processing         |
| NumPy                   | Numerical operations    |
| Scikit-learn            | Machine Learning        |
| CountVectorizer         | Text feature extraction |
| Multinomial Naive Bayes | Spam classification     |
| Matplotlib              | Data visualization      |
| Seaborn                 | Visualization           |
| WordCloud               | Spam word visualization |
| Jupyter Notebook        | Development environment |

---

## 📂 Dataset

The project uses a **spam/ham message dataset** containing text messages and their corresponding categories.

The dataset contains columns including:

* `v1` — message category
* `v2` — message text

During preprocessing, these columns are renamed to:

```text
Category
Message
```

A binary `Spam` column is then created:

```text
1 → Spam
0 → Ham
```

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Exploration
   ↓
Duplicate & Missing Value Checking
   ↓
Data Cleaning
   ↓
Spam / Ham Classification
   ↓
Word Cloud Visualization
   ↓
Train-Test Split
   ↓
CountVectorizer
   ↓
Multinomial Naive Bayes
   ↓
Model Prediction
   ↓
Model Evaluation
   ↓
Spam Detection
```

---

## 🧠 Machine Learning Pipeline

The project uses a Scikit-learn Pipeline combining:

```python
clf = Pipeline([
    ('vectorizer', CountVectorizer()),
    ('nb', MultinomialNB())
])
```

The pipeline performs two major steps:

### 1. CountVectorizer

Converts text messages into numerical word-count features.

### 2. Multinomial Naive Bayes

Uses the extracted text features to classify the message as spam or ham.

---

## 📊 Model Evaluation

The model evaluation includes:

### Accuracy

Measures the overall percentage of correctly classified messages.

### Precision

Measures how many messages predicted as spam are actually spam.

### Recall

Measures how many actual spam messages are correctly detected.

### F1-Score

Provides a balance between precision and recall.

### ROC-AUC

Measures the classification performance using the ROC curve.

### Confusion Matrix

The confusion matrix shows:

```text
True Positive
True Negative
False Positive
False Negative
```

---

## ☁️ Spam Word Cloud

The project generates a Word Cloud using messages classified as spam.

It helps visualize frequently occurring words in spam messages.

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/email-spam-detection.git
```

### 2. Navigate to the Project

```bash
cd email-spam-detection
```

### 3. Install Required Libraries

```bash
pip install numpy pandas matplotlib seaborn scikit-learn wordcloud
```

### 4. Open the Notebook

Open:

```text
Email_spam_detection_wih_ML.ipynb
```

using Jupyter Notebook, JupyterLab, or another compatible notebook environment.

### 5. Run the Cells

Run the notebook cells sequentially to:

1. Load the dataset
2. Explore the data
3. Clean the dataset
4. Create the spam labels
5. Visualize spam messages
6. Train the model
7. Evaluate the model
8. Test new messages

---

## 🧪 Example Predictions

The project includes examples such as:

```python
sample_email = 'Free Tickets for IPL'
result = detect_spam(sample_email)
print(result)
```

and:

```python
sample_email = 'offer of 1000'
result = detect_spam(sample_email)
print(result)
```

The trained classifier returns either:

```text
This is a Spam Email!
```

or:

```text
This is a Ham Email!
```

---

## 📁 Project Structure

```text
Email-Spam-Detection/
│
├── Email_spam_detection_wih_ML.ipynb
├── spam.csv
├── README.md
└── requirements.txt
```

> The exact repository structure may vary depending on how the project is uploaded to GitHub.

---

## 🔮 Future Scope

The project can be further improved by:

* Using TF-IDF instead of only word counts.
* Testing additional Machine Learning algorithms.
* Applying advanced NLP preprocessing.
* Using deep-learning models for text classification.
* Creating a web application using Flask or FastAPI.
* Creating an email-integrated spam filtering system.
* Adding a user-friendly interface for real-time predictions.
* Improving detection of new and previously unseen spam patterns.

---

## ⚠️ Disclaimer

This project is developed for **educational and demonstration purposes**. Machine Learning predictions may not always be correct, and legitimate messages can sometimes be incorrectly classified as spam.

---

## 👨‍💻 Author

**Manish Jaiswal**

B.Tech — Artificial Intelligence & Machine Learning

---

## ⭐ Project

If you find this project useful for learning **Machine Learning, NLP, and text classification**, consider giving the repository a ⭐.
