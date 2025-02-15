# IMDB-Movie-Recommendation-System-Using-Storylines

1. Introduction:
```
This project involves building a movie recommendation system based on IMDb movies released in 2024. The system extracts movie titles and descriptions from IMDb, processes the data, and uses TF-IDF (Term Frequency-Inverse Document Frequency) with cosine similarity to suggest similar movies based on a given storyline.
```

2. Technology Stack:
```
* Web Scraping: Selenium
* Data Processing: Pandas, NumPy
* Natural Language Processing: NLTK, Scikit-learn (TF-IDF)
* Machine Learning: Cosine Similarity (Scikit-learn)
* Frontend: Streamlit
```

3. Workflow:
```
Step 1: Web Scraping IMDb Data
* Objective: Extract movie titles and descriptions for 2024 releases from IMDb.
* Tool Used: Selenium
* Process:
i) Load the IMDb search page for movies released in 2024.
ii) Click on the Load More button until all movies are visible.
iii) Extract movie titles and descriptions.
iv) Save the data in a CSV file (imdb_movies_2024.csv).

Step 2: Data Preprocessing
* Objective: Clean and prepare movie descriptions for text similarity computation.
* Steps:
i) Convert text to lowercase.
ii) Remove punctuation and numbers.
iii) Tokenize text and remove stopwords.
iv) Store cleaned descriptions for further processing.

Step 3: Feature Engineering
* Model Used:
- TF-IDF (Term Frequency - Inverse Document Frequency): Converts movie descriptions into a numerical feature vector.
* Tool Used: Scikit-learn’s TfidfVectorizer
* Steps:
i) Use TfidfVectorizer to transform cleaned movie descriptions into TF-IDF vectors.
ii) Store the transformed matrix for similarity calculations.

Step 4: Computing Cosine Similarity
* Objective: Measure similarity between input storyline and all movies.
* Tool Used: Scikit-learn’s cosine_similarity
* Process:
i) Compute cosine similarity matrix for all movies.
ii) When a user inputs a storyline, transform it using the same TF-IDF vectorizer.
iii) Compute similarity scores and return the top 5 most similar movies.

Step 5: Streamlit Web Application
* Objective: Provide an interactive UI for users to enter a storyline and get movie recommendations.
* Process:
i) Load IMDb data and precompute TF-IDF matrix.
ii) Provide a text area for users to enter a storyline.
iii) Compute movie recommendations based on cosine similarity.
iv) Display results with titles, descriptions, and similarity scores.
```

4. Results and Evaluation:
```
* Data Collected: Extracted titles and descriptions of all IMDb 2024 movies.
* TF-IDF Model: Successfully transformed descriptions into numerical vectors.
* Manual Verification:
- Tested with various plot descriptions and manually verified recommendations.
* Recommendation Accuracy: Provides relevant movie suggestions based on input storyline.
* Consistency Check:
- Given the same input, results remain consistent across multiple runs.
* Performance:
- TF-IDF vectorization is fast, and cosine similarity lookup is efficient.
- Efficiently retrieves recommendations within seconds.
```

5. Challenges & Future Improvements:
```
Challenges:
* IMDb’s dynamic loading mechanism required handling Load More clicks effectively.
* Data inconsistency in movie descriptions affected cleaning quality.

Future Improvements:
* Implement deep learning models (BERT, Transformers) for improved similarity detection.
* Add user ratings and genre-based filtering for better recommendations.
* Improve UI/UX with enhanced visualization of movie results.
```

6. Conclusion:
```
This project successfully developed a movie recommendation system based on text similarity analysis of IMDb movie descriptions. It provides an interactive experience for users to discover similar movies based on storyline input.
```
