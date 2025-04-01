# CA05: kNN-Based Movie Recommender Engine

## Project Overview
This project implements a k-Nearest Neighbor based movie recommender system. The primary goal is to recommend the top 5 most similar mvoies to a given movie based on the genre and IMDB rating.

## Dataset Description
The dataset used is obtained from the UCI Machine Learning Repository:

- File Name: movies_recommendation_data.csv
- Source URL:
  https://github.com/ArinB/MSBA-CA-Data/raw/main/CA05/movies_recommendation_data.csv
- Description: Contains 30 movies with attributes such as IMDB rating and encoded genre indicators (Biography, Drama, Thriller, Comedy, Crime, Mystery).

## Necessary Packages and Libraries
To successfully run the notebook, make sure you have the following libraries installed:
- pandas
- numpy
- matplotlib
- scikit-learn

You can install the necessary libraries using pip:
```
pip install pandas numpy matplotlib scikit-learn
```

## Methodology and Steps
1. Data Loading and Preparation:
    - Load the data from the specified URL.
    - Remove any unecessary columns (i.e. "Label" column)

2. Data Preprocessing
    - Checked for binary encoding (0 or 1) in genre columns.
    - Scaled the IMDB ratings using MinMaxScaler for uniformity.

3. Build the kNN Model
    - Used sklearn.neighbors.NearestNeighbors with Euclidean distance (most commonly used metric).
    - Set number of neighbors to 5, to provide 5 nearest movie recommendations. 

4. Querying the Model
    - The test movie is "The Post" with the following attributes: 
        - IMDB Rating: 7.2 (requires scaling)
        - Genres: Biography (1), Drama (1), Thriller (0), Comedy (0), Crime (0), Mystery (0), History (redacted)

5. Generating REcommendations 
    - The model predicts the top 5 most similar movies. 
    - The recommendations are displayed with their titles, and includes distance from the query movie for assignment demonstration purposes. 

## Notes
- The model uses Euclidean distance as it best fits the combination of binary and scaled numerical data. 
- *Warning*: "x does not have valid feature names" can occur if the test movie vector does not match the structure of the trained data. To resolve, ensure the query movie is formatted as a DataFrame with correct column names. 
