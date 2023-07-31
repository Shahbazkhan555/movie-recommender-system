# Movie Recommender System App

## Demo Video

![Movie Recommender System Demo](movie-recommender-demo.gif)


## Overview

The Movie Recommender System App is a content-based movie recommendation application that suggests movies to users based on their interests. It utilizes the Bags of Words (BoW) technique and Cosine Similarity to find similarities between movies and recommend those that are most relevant to the user's preferences.

The application uses data from the "TMDB 5000 MOVIES DATASET," which is sourced from Kaggle, to build its movie recommendation model. Additionally, the app fetches movie posters from the TMDb API to enhance the user experience.

## How It Works

The Movie Recommender System App operates as follows:

1. **Bags of Words (BoW) Technique**: The application processes the movie plots (synopsis) in the dataset and uses the BoW technique to convert the text data into numerical feature vectors. This representation allows the system to compute the similarity between movie plots based on the frequency of words.

2. **Cosine Similarity**: After converting the movie plots into BoW feature vectors, the app calculates the cosine similarity between each pair of movies. Cosine similarity measures the cosine of the angle between two vectors, indicating their similarity.

3. **Content-Based Recommendation**: The app takes user input in the form of a movie title or keyword and identifies the most similar movies based on the BoW and cosine similarity calculations. It then generates a list of recommended movies and displays them to the user.

4. **Movie Posters from TMDb API**: To enrich the user interface, the app fetches movie posters from the TMDb API corresponding to the recommended movies. These posters are displayed alongside the movie titles, allowing users to identify movies visually.

## Data Preparation

To execute the Movie Recommender System App, follow these steps:

1. Run the `notebook.ipynb` file to perform data preprocessing and similarity calculations. The notebook will generate two important files:

   - `similarity.pkl`: This file contains the cosine distances between movie plots, saved in vector form, used for similarity calculations.

   - `movie_dict.pkl`: This file is generated by converting the preprocessed DataFrame into a dictionary form, essential for quick retrieval in the recommendation app.

2. After running the notebook and obtaining the necessary files, execute `app.py` to launch the Streamlit web application. Make sure to have all dependencies installed (specified in `requirements.txt`).


## Installation and Usage

To run the Movie Recommender System App on your local machine, follow these steps:

1. Clone the repository to your local machine:

   ```
   git clone https://github.com/YourUsername/movie-recommender-system.git
   ```

2. Install the required dependencies. It is recommended to use a virtual environment:

   ```
   cd movie-recommender-system
   pip install -r requirements.txt
   ```

3. Obtain an API key from the TMDb website (https://www.themoviedb.org/) and update the `config.py` file with your API key.

4. Execute `notebook.ipynb` to generate `similarity.pkl` and `movie_dict.pkl`.

5. Run the Streamlit app:

   ```
   streamlit run app.py
   ```

6. Access the application in your web browser at `http://localhost:8501`.

## Acknowledgments

- The "TMDB 5000 MOVIES DATASET" used in this project is sourced from Kaggle (https://www.kaggle.com/tmdb/tmdb-movie-metadata).

- The application makes use of the TMDb API (https://www.themoviedb.org/documentation/api) to fetch movie posters and enhance the user experience.

## Feedback and Contributions

Feedback and contributions to the Movie Recommender System App are welcomed! Feel free to open an issue or submit a pull request with any suggestions or improvements you'd like to see.

Happy movie recommendation! 🎬🍿