# Content-Based Movie Recommendation System

This project implements a movie recommendation engine using **content-based filtering** on the TMDB 5000 Movies and Credits datasets. It recommends similar movies based on features such as genres, keywords, cast, crew, and plot descriptions — without relying on user ratings.

---

## Overview

Movies are represented using textual metadata which is preprocessed using NLP techniques. These processed features are vectorized using `CountVectorizer`, and similarity between movies is computed using **cosine similarity**.

---

## Key Features

- Merged and cleaned TMDB movies and credits datasets
- Feature extraction from: `genres`, `keywords`, `cast`, `crew`, and `overview`
- Applied text preprocessing (stemming, lowercasing, stopword removal)
- Vectorized using `CountVectorizer` (Bag-of-Words model)
- Cosine similarity used to compute movie-to-movie closeness
- `recommend("Movie Title")` function returns top 5 similar movies
-  Optional: Poster fetching using the TMDB API (API key hidden for security)

---

## How to Run

1. Clone the repository or download the files.
2. Open `ML_content_based_movie_recommendation.ipynb` using Jupyter Notebook or VS Code.
3. Run all cells in order to:
   - Preprocess the data
   - Train the vector space model
   - Test recommendations
4. Call `recommend('Inception')` or any other movie title.

---

## Tech Stack

- Python 3.x
- Pandas, NumPy
- NLTK
- Scikit-learn
- Jupyter Notebook
- Requests (for optional poster API)

---

## Note on API Key

If you wish to enable poster fetching from the TMDB API:

1. Create a `.env` file with your API key:
   ```
   TMDB_API_KEY=your_api_key_here
   ```
2. Use `os.getenv("TMDB_API_KEY")` to access it safely.

---

## Author

**Harshavardhan Renjarla**  

---

## License

This project is licensed under the MIT License – feel free to use and adapt with attribution.
