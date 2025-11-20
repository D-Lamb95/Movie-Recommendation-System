🎬 Movie Recommendation System

A content-based recommender using movie genres

Overview

This project builds a content-based movie recommendation system using movie metadata from the MovieLens dataset. The goal is to recommend movies that are similar based on shared genres. Unlike collaborative filtering, which relies on user behaviors, this approach recommends films by analyzing the content of each movie directly.

The system transforms genre information into a structured format and computes similarity scores between all movies. Users can enter a movie title and receive recommendations of films with similar characteristics.

Data Description

The dataset includes two primary files:

  -   movies.csv – Contains movie titles, unique IDs, and genre labels

  -   ratings.csv – Contains user ratings for each movie

Movies typically have genre strings such as:
Adventure|Children|Fantasy
These are split and converted into binary indicator columns so each movie can be compared based on genre composition.

The recommendation system uses these encoded genres to match similar films.

Methods

To build the recommender:

  -  Movie and rating datasets were merged using movieId.

  - Genres were one-hot encoded to create a matrix indicating which genres each movie belongs to.

  -  Cosine similarity was calculated between all movie vectors to measure how similar each pair of films is.

A function was created to retrieve the top recommended titles based on the similarity scores.

This approach ensures that movies with similar thematic or categorical elements appear in the results.

Example

When a user enters a movie such as “Jumanji (1995)”, the system identifies films with similar genre patterns, returning results such as:

  -  The Indian in the Cupboard (1995)

  -  The NeverEnding Story III (1994)

  -  Escape to Witch Mountain (1975)

  -  Return to Oz (1985)

These recommendations reflect shared attributes such as family-friendly themes or adventure and fantasy elements.

Requirements

To run the notebook or script, the following Python libraries are required:

  -  pandas

  -  numpy

  -  scikit-learn

These can be installed with:
