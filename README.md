# 💼 Glassdoor Salary Prediction
[![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange)](https://jupyter.org/)
[![View on NBViewer](https://img.shields.io/badge/View%20Notebook-NBViewer-brightgreen)](https://nbviewer.org/github/yourusername/reponame/blob/main/Copy_of_Sample_ML_Submission_Template.ipynb)

---

A Machine Learning project that predicts salary estimates for job postings using structured data and natural language processing (NLP) on job descriptions. Built using various ensemble models, feature selection techniques, and NLP pipelines to improve prediction accuracy.

---

## 📌 Project Objective

The objective of this project is to **predict the average salary** for job listings on Glassdoor using:
- **Job-related attributes** (e.g., job title, location, size, ownership)
- **Company-specific features** (e.g., revenue, ratings, age)
- **Textual features** from job descriptions (via TF-IDF)

This helps:
- Job seekers assess fair salary expectations
- Recruiters and analysts benchmark roles more accurately

---

## 📊 Dataset Overview

**Source:** Glassdoor Jobs Dataset (2017–2018)  
**File:** `glassdoor_jobs.csv`

Key features include:
- `Job Title`
- `Salary Estimate`
- `Job Description`
- `Rating`, `Size`, `Revenue`, `Type of ownership`, `Industry`, `Sector`, etc.

Target variable: `avg_salary` (engineered from the raw salary estimates)

---

## 🛠️ Workflow

### 1. 🧹 Data Cleaning
- Removed rows with missing/null salary data
- Cleaned salary text to extract min, max, and average values
- Engineered new features: `Company Age`, `Has_Competitor`, etc.

### 2. 📊 Exploratory Data Analysis (EDA)
- Visualized job distribution by title, location, sector
- Correlation heatmaps
- Salary trends vs. company ratings and industry

### 3. 🧠 Feature Engineering
- Label encoding and one-hot encoding of categorical features
- TF-IDF vectorization on `Job Description`
- `SelectKBest` used to retain top features

### 4. 🧪 Model Building
- Trained several models:
  - **Random Forest Regressor**
  - **XGBoost Regressor**
  - **Stacking Ensemble**
- Final model saved as:
  - `best_model_joblib.pkl`
  - `best_xgboost_model.pkl`

### 5. 📦 Saved Artifacts
- `tfidf_vectorizer.pkl`: Vectorizer for job descriptions
- `select_kbest.pkl`: Feature selector object
- `onehot_columns.pkl`, `selected_kbest_columns.pkl`: Encoded column references

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/Pavan-Kumar-Dirisala/Glassdoor-Salary-Prediction.git
cd Glassdoor-Salary-Prediction


# 2. Run the Jupyter Notebook
jupyter notebook Sample_ML_Submission_Template.ipynb
```
## 📂 Repository Structure
```yml
Glassdoor-Salary-Prediction/
│
├── glassdoor_jobs.csv
├──Sample_ML_Submission_Template.ipynb
├── best_model_joblib.pkl
├── best_xgboost_model.pkl
├── tfidf_vectorizer.pkl
├── select_kbest.pkl
├── onehot_columns.pkl
├──selected_kbest_columns.pkl
```

# 🧰 Tech Stack

## 🖥️ Languages
- Python

## 📚 Libraries
- pandas, numpy
- scikit-learn
- xgboost, lightgbm
- matplotlib, seaborn
- joblib, pickle

## 🧠 NLP
- TF-IDF Vectorizer
- SelectKBest for Dimensionality Reduction

## 🙋‍♂️ Author

Pavan Kumar Dirisala
- 📧 dirisalapavankumar12@gmail.com
- 🎓 KL University | CSE - AI & IP
- 🌐 GitHub: [[Pavan-Kumar-Dirisala]](https://github.com/Pavan-Kumar-Dirisala)

## ⭐ Future Improvements

- Deploy model via Streamlit or Flask
- Add real-time scraping of new job listings
- Integrate BERT-based NLP models on descriptions
