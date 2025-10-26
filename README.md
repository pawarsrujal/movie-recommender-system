🎬 Movie Recommendation System
📖 Overview

The Movie Recommendation System is a machine learning project that recommends movies similar to the one a user selects.
It uses content-based filtering to analyze the similarity between movies based on their features such as genres, cast, director, keywords, and storyline overview.

This project combines a Jupyter Notebook backend (for building and training the recommendation model) with a Streamlit-based frontend web app that provides an intuitive, interactive interface for users.

🚀 Project Workflow
🔹 Step 1: Data Collection
The dataset used in this project contains metadata about movies, including:
Title
Overview (movie plot description)
Genre
Cast
Crew (especially director)
Keywords
Data is usually taken from TMDB (The Movie Database) or Kaggle’s movie metadata dataset.


🔹 Step 2: Data Preprocessing
The data is cleaned and processed to make it suitable for analysis:
Handling missing values
Selecting relevant features
Combining multiple textual columns (like genres, cast, director) into a single “tags” column
Converting text to lowercase and removing stopwords


🔹 Step 3: Feature Extraction
To allow comparison between movies, textual data is converted into numerical form using:
CountVectorizer or TfidfVectorizer (from scikit-learn)
This creates a feature matrix where each row represents a movie, and each column represents a word feature.


🔹 Step 4: Similarity Computation
We compute Cosine Similarity between all movie vectors.
The cosine similarity value determines how close two movies are in terms of their feature vectors.
When a user selects a movie, the system retrieves and ranks other movies with the highest similarity scores.


🔹 Step 5: Streamlit Frontend
The frontend is built using Streamlit, which provides:
A simple text box for the user to input or select a movie title.
A “Recommend” button that triggers the recommendation function.
A clean display of the top 5 similar movies (with optional posters or titles).

