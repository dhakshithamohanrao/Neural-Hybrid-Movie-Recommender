# Neural-Hybrid-Movie-Recommender

## Description

This project implements a **hybrid movie recommendation system** combining content-based filtering and a neural collaborative filtering model (NeuMF) using the MovieLens small dataset.

* **Content-based Filtering:** Uses movie titles and genres to create embeddings with SentenceTransformers and recommends similar movies based on cosine similarity.
* **Neural Collaborative Filtering:** Trains a NeuMF model using user-movie ratings with negative sampling to predict personalized recommendations.
* **Hybrid Recommendations:** Combines content-based and neural CF results to provide enhanced, diverse movie suggestions.

The system supports generating top-N movie recommendations for a given user or based on a particular movie. It also includes evaluation metrics such as **Hit Ratio (HR)** and **NDCG** to measure recommendation quality.

## Features

* Preprocesses MovieLens data for content-based and collaborative filtering.
* Generates semantic movie embeddings for content-based recommendations.
* Implements NeuMF neural network for user-specific recommendation predictions.
* Supports hybrid recommendation combining content and collaborative approaches.
* Evaluates model performance using HR@K and NDCG@K metrics.

