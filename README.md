# Product_Review_Sentiment_Analysis

## Project Overview

**Product Review Sentiment Analysis** is an NLP and Machine Learning project that analyzes customer product reviews and classifies them into **Positive, Neutral, or Negative** sentiments.

The project uses a pre-trained **Sentence Transformer (`all-MiniLM-L6-v2`)** to convert reviews into meaningful numerical embeddings. These embeddings are then used to train machine learning classification models.

---

## Objectives

* Analyze and preprocess customer product reviews.
* Perform Exploratory Data Analysis (EDA).
* Convert text reviews into embeddings using Sentence Transformers.
* Train machine learning classification models.
* Compare model performance using Accuracy and F1 Score.
* Select the best-performing model.

---

## Dataset

The dataset contains **1,007 product reviews** with the following columns:

| Column           | Description                    |
| ---------------- | ------------------------------ |
| `Product ID`     | Unique product identifier      |
| `Product Review` | Customer's written review      |
| `Sentiment`      | Positive, Neutral, or Negative |

Duplicate records were identified and removed during preprocessing.

---

## Exploratory Data Analysis

The sentiment distribution was analyzed to understand the customer feedback.

The dataset contains more **positive reviews** compared with neutral and negative reviews. Because of this class imbalance, **Weighted F1 Score** was considered along with accuracy during model evaluation.

---

## Methodology

```text
Customer Reviews
       ↓
Data Cleaning
       ↓
Exploratory Data Analysis
       ↓
Sentence Transformer
       ↓
Text Embeddings
       ↓
Train-Test Split
       ↓
Machine Learning Models
       ↓
Model Evaluation
       ↓
Best Model Selection
```

### Sentence Transformer

The pre-trained **`all-MiniLM-L6-v2`** model was used to generate numerical embeddings from the product reviews.

These embeddings capture the semantic meaning of the text and are used as input features for the classification models.

---

## Machine Learning Models

### Random Forest Classifier

Random Forest uses multiple decision trees to make predictions.

**Performance:**

* Accuracy: **~86.5%**
* Weighted F1 Score: **~81.8%**

### Gradient Boosting Classifier

Gradient Boosting builds models sequentially to improve prediction performance.

**Performance:**

* Accuracy: **~84.1%**
* Weighted F1 Score: **~80.3%**

### Model Comparison

| Model                           |   Accuracy | Weighted F1 Score |
| ------------------------------- | ---------: | ----------------: |
| **Random Forest + Transformer** | **~86.5%** |        **~81.8%** |
| Gradient Boosting + Transformer |     ~84.1% |            ~80.3% |

**Random Forest + Sentence Transformer embeddings** achieved the best overall performance.

---

## Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Sentence Transformers**
* **Google Colab / Jupyter Notebook**

---

## Project Structure

```text
Product-Review-Sentiment-Analysis/
│
├── Product_Review_Sentiment_Analysis.ipynb
├── Product_Reviews.csv
└── README.md
```

---

## How to Run

### 1. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn sentence-transformers
```

### 2. Open the notebook

Open `Product_Review_Sentiment_Analysis.ipynb` using **Google Colab** or **Jupyter Notebook**.

### 3. Load the dataset

Update the dataset path according to your environment.

### 4. Run the notebook

Execute the cells sequentially to perform preprocessing, generate embeddings, train the models, and evaluate their performance.

---

## Future Improvements

* Fine-tune Transformer models for sentiment classification.
* Experiment with XGBoost and SVM.
* Perform hyperparameter tuning.
* Improve handling of class imbalance.
* Increase the size and diversity of the dataset.
* Deploy the sentiment prediction model using **Streamlit**.

---

## Key Learnings

This project provided practical experience in:

* Natural Language Processing
* Text classification
* Transformer-based embeddings
* Exploratory Data Analysis
* Machine Learning
* Model evaluation and comparison

---

