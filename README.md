# Neural-Hybrid-Movie-Recommender

[![Python](https://img.shields.io/badge/Python-3.9+-blue)](https://www.python.org/)  
[![PyTorch](https://img.shields.io/badge/PyTorch-1.13+-orange)](https://pytorch.org/)  
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

A **hybrid movie recommendation system** that combines **content-based filtering** with **Neural Collaborative Filtering (NeuMF)** to provide accurate and personalized movie recommendations.

---

## Features

- **Content-based filtering:** Recommends movies similar to a given movie using metadata (title + genres) and embeddings from `sentence-transformers`.  
- **Neural Collaborative Filtering (NeuMF):** Trains a neural network on user ratings to predict preferences.  
- **Hybrid recommendations:** Combines both approaches for improved accuracy.  
- **Evaluation metrics:** Uses Hit Ratio (HR) and Normalized Discounted Cumulative Gain (NDCG) for performance measurement.  

---

## Tech Stack

- Python 3.x  
- PyTorch  
- Pandas, NumPy, Scikit-learn  
- Sentence Transformers (`all-MiniLM-L6-v2`)  

---

## Dataset

- [MovieLens ml-latest-small](https://grouplens.org/datasets/movielens/latest/)  
- Contains `movies.csv`, `ratings.csv`, and `links.csv`.

---

## Installation

1. Clone the repository:  
```bash
git clone https://github.com/<your-username>/Neural-Hybrid-Movie-Recommender.git
cd Neural-Hybrid-Movie-Recommender
```

2. Install dependencies:  
```bash
pip install -r requirements.txt
```

3. Run the notebook or Python script:  
```bash
jupyter notebook
```
or
```bash
python main.py
```

---

## Usage

### Content-based Recommendation
```python
recommend_movie("Toy Story (1995)", top_n=5)
```

### Neural Collaborative Filtering (NeuMF) Recommendation
```python
recommend_ncf(user_id=1, top_n=5)
```

### Hybrid Recommendation
```python
hybrid_recommend(user_id=1, movie_title="Toy Story (1995)", top_n=5)
```

---

## Evaluation Metrics

- **Hit Ratio (HR):** Measures whether the true positive movie appears in top-N recommendations.  
- **Normalized Discounted Cumulative Gain (NDCG):** Evaluates ranking quality by considering the position of the true positive movie.  

---

## Results

After training on the MovieLens dataset:  

**Top 5 recommendations for User 1:**  
```
1. Toy Story 2 (1999)
2. Jumanji (1995)
3. Grumpier Old Men (1995)
4. Heat (1995)
5. Father of the Bride Part II (1995)
```

**Hybrid recommendations for User 1 (based on Toy Story):**  
```
1. Toy Story 2 (1999)
2. A Bug's Life (1998)
3. Monsters, Inc. (2001)
4. Jumanji (1995)
5. Toy Story 3 (2010)
```

---

