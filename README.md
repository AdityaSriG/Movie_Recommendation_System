# 🎬 Movie Recommendation System

A simple **content-based movie recommendation system** built using **NLP techniques** and **Cosine Similarity**.  
This project uses the [TMDB 5000 Movies Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata) to recommend similar movies based on their **overview, genres, keywords, cast, and crew**.

---

## 🚀 Features
- Extracts and processes movie metadata (genres, keywords, cast, crew, overview).
- Combines features into a single **tags column**.
- Applies **text preprocessing**:
  - Tokenization  
  - Lowercasing  
  - Stemming (Porter Stemmer)  
  - Stopwords removal  
- Builds feature vectors using **Bag of Words (CountVectorizer)**.
- Uses **Cosine Similarity** to find and recommend the most similar movies.

---

## 📂 Dataset
- **tmdb_5000_movies.csv**
- **tmdb_5000_credits.csv**

Dataset source: [Kaggle - TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

---

## ⚙️ Tech Stack
- **Python** 🐍
- **Libraries**: 
  - NumPy, Pandas, Seaborn  
  - NLTK (Natural Language Toolkit)  
  - Scikit-learn (CountVectorizer, Cosine Similarity)  

---

## 📖 How It Works
1. Merge `movies` and `credits` dataset.
2. Extract relevant features: `movie_id, title, overview, genres, keywords, cast, crew`.
3. Convert JSON-like fields into lists (using `ast.literal_eval`).
4. Create a new `tags` column by combining text features.
5. Apply NLP preprocessing (lowercasing, stemming, etc.).
6. Convert text into vectors with **CountVectorizer**.
7. Compute similarity matrix using **Cosine Similarity**.
8. Build a function `recommend(movie)` to suggest top 5 similar movies.

---

## 🛠️ Installation & Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/movie-recommender.git
   cd movie-recommender
