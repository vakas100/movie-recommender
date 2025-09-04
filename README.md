# Movie Recommendation System (Draft)

This project builds a simple **content-based movie recommendation system** using the **TMDB 5000 Movies Dataset**.  
It recommends movies similar to a given movie by comparing features like genres, keywords, cast, crew, and overview.  

---

## Features
- Preprocesses and cleans movie + credits datasets.  
- Extracts important details: **genres, keywords, cast, crew, overview**.  
- Creates a combined `tags` column for each movie.  
- Uses **CountVectorizer** (Bag of Words) to convert text into numbers.  
- Computes similarity with **cosine similarity**.  
- Returns **top 5 recommendations** for a given movie.  

---

## Dataset
- `tmdb_5000_movies.csv`  
- `tmdb_5000_credits.csv`  

These contain movie metadata like id, title, cast, crew, genres, keywords, and overview.  

---

## Tech Stack
- Python  
- Pandas, NumPy  
- NLTK (PorterStemmer)  
- scikit-learn (CountVectorizer, cosine similarity)  

---

## Workflow (Simplified)
1. Merge movies + credits datasets.  
2. Clean data and handle missing values.  
3. Convert stringified JSON (`genres`, `keywords`, `cast`, `crew`) into lists.  
4. Extract top actors and director, split overview into words.  
5. Normalize text (lowercase, remove spaces, stemming).  
6. Create `tags` column combining all features.  
7. Vectorize text with CountVectorizer.  
8. Compute similarity with cosine similarity.  
9. Build a recommend function that returns top 5 similar movies.  

---


