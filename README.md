# Recommender-Systems---Movies
# Movie Recommendation System with User-Based Collaborative Filtering and SVD

## Overview

This project implements a movie recommendation system using two popular collaborative filtering techniques: User-Based Collaborative Filtering and Singular Value Decomposition (SVD). The goal is to predict which movies a user might like and recommend the top 10 movies for each user. The recommendation accuracy is evaluated using Mean Average Precision at 10 (MAP@10).

## Dataset

The project utilizes a dataset where each row represents a movie rating given by a user. The dataset includes the following columns:

•   `userId`: Unique identifier for each user.
•   `movieId`: Unique identifier for each movie.
•   `rating`: The rating given by the user to the movie.
•   `timestamp`: Timestamp of the rating.
•   `title`: Title of the movie.

'https://raw.githubusercontent.com/aiedu-courses/stepik_applied_tasks/main/datasets/movies_ratings.csv'

## Methods

This recommendation system employs the following two approaches:

1.  **User-Based Collaborative Filtering:**

    •   **Concept:** Recommends movies to a user based on the preferences of other users who have similar taste.
    •   **Implementation:**
        *   Calculates user similarity based on their rating patterns.
        *   Identifies the *k* most similar users for a given user.
        *   Predicts the rating of a movie for a user by aggregating the ratings of similar users, weighted by their similarity scores.
        *   Recommends the top 10 movies with the highest predicted ratings.

2.  **Singular Value Decomposition (SVD):**

    •   **Concept:** Reduces the dimensionality of the user-movie rating matrix to extract latent features that represent the underlying preferences of users and the characteristics of movies.
    •   **Implementation:**
        *   Decomposes the user-movie rating matrix into three matrices.
        *   Reduces the dimensionality by keeping only the top *k* singular values (and corresponding singular vectors).
        *   Reconstructs an approximation of the original rating matrix using the reduced matrices.
        *   Predicts missing ratings based on the reconstructed matrix.
        *   Recommends the top 10 movies with the highest predicted ratings.

## Evaluation Metric

The performance of the recommendation systems is evaluated using **Mean Average Precision at 10 (MAP@10)**.  This metric measures the average precision of the top 10 recommended items for each user.

## Usage

1.  Clone the repository: `git clone `
2.  Install the required dependencies: `pip install -r requirements.txt`
3.  Run the main script: `python main.py`

## Dependencies

•   NumPy
•   Pandas
•   Scikit-learn
•   Matplotlib
•   tqdm

## Future Work

•   Explore hybrid recommendation approaches that combine collaborative filtering and content-based filtering.
•   Implement a cold-start strategy to handle new users or movies with limited ratings.
•   Tune the number of latent features *k* in SVD to optimize performance

