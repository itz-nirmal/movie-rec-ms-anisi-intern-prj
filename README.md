# 🎬 Movie Recommendation System - MS-ANISI Internship Project

This is a **Content-Based Movie Recommender System** developed using **Python** and **Flask**, as part of an internship project at MS-ANISI. The system recommends movies based on textual similarity using **TF-IDF vectorization** and **Cosine Similarity**.

> 🔗 GitHub Repository: [itz-nirmal/movie-rec-ms-anisi-intern-prj](https://github.com/itz-nirmal/movie-rec-ms-anisi-intern-prj)

---

## 📌 Overview

This recommender analyzes a given movie's metadata and recommends similar movies from the dataset. If a movie title is not found, the system suggests approximate matches using JavaScript-based fuzzy logic.

---

## 🧠 Recommendation Logic

### 📈 Feature Extraction — TF-IDF

- We use **Term Frequency-Inverse Document Frequency (TF-IDF)** to vectorize movie metadata.
- TF-IDF transforms textual features into numerical vectors in a **Vector Space Model (VSM)**, which represents the relevance of terms.

### 📐 Similarity Metric — Cosine Similarity

- **Cosine Similarity** calculates the angle between vectors to determine similarity.
- This metric is ideal for comparing text documents of different lengths, making it suitable for our movie data.

---

## 💻 Code Components

### 🐍 Python (`app.py`)

- Loads and processes the dataset (`tmdb.csv`)
- Uses `scikit-learn` to compute TF-IDF vectors and cosine similarities
- Hosts a Flask web server to accept user input and return recommendations
---

## ⚙️ Setup Instructions

### 🔧 Local Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/itz-nirmal/movie-rec-ms-anisi-intern-prj.git
   cd movie-rec-ms-anisi-intern-prj
2. **Create and activate virtual environment**
   ```bash
   python -m venv venv
# Activate:
1. **On Windows**:
   ```bash
   .\venv\Scripts\activate
2. **On macOS/Linux:**
   ```bash
   source venv/bin/activate
3. **Install dependencies & run**
   ```bash
   pip install -r requirements.txt
   set FLASK_APP=app.py
   set FLASK_ENV=development
   flask run
