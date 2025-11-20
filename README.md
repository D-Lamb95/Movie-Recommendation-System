🎬 Movie Recommendation System (Content-Based)

This project builds a content-based movie recommender system using the MovieLens dataset.
The system recommends movies based on genre similarity, using a cosine similarity matrix built from one-hot encoded genre features.

It is a simple and intuitive approach to building a recommendation engine without requiring user history or ratings predictions.

📌 Project Overview

This project:

Loads movie metadata (movies.csv) and user ratings (ratings.csv)

Merges both datasets on movieId

Converts the genres column into a binary matrix (one-hot encoding)

Computes cosine similarity between all movies

Includes a function recommend_movies() that returns the top recommended titles based on a movie you provide

📂 Dataset Requirements

Place these two files in the project directory:

movies.csv

movieId

title

genres (pipe-separated, e.g., Adventure|Children|Fantasy)

ratings.csv

userId

movieId

rating

timestamp

These datasets are merged so genre and title information is aligned with rating data.

🧠 Core Logic
1. Load datasets
