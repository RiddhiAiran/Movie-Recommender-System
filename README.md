# Content-Based Movie Recommender System

This project is a **Content-Based Movie Recommender System** that suggests movies based on content similarity to a user-selected movie. It uses **Cosine Similarity** to find similarities between movies and recommend the most similar ones.

## DEMO
![Movie Recommender Working Demo](https://github.com/user-attachments/assets/cf05c4ae-cc77-4264-a29d-6f8aff1874b0)


## Project Overview

The system allows users to input a movie title, and it will recommend 5 movies with similar content. The recommendations are shown with their titles and movie posters. This recommender system leverages the `Cosine Similarity` technique to measure the similarity between movies based on their features.

### Key Features:
- **Cosine Similarity**: Measures the similarity between movies based on their content (e.g., genres, descriptions).
- **Movie Poster Display**: Shows a poster for each recommended movie.
- **Interactive Interface**: Built with Streamlit for a smooth user experience.

## How It Works

1. The movie data (titles, movie IDs, etc.) and precomputed similarity matrix are loaded from two pickle files: `movie_list.pkl` and `similarity.pkl`.
2. When the user selects a movie from the dropdown list, the system fetches the most similar movies based on the cosine similarity score.
3. The recommended movies are displayed with their titles and corresponding movie posters.

## Requirements

To run this project, you'll need to install the following dependencies:

- `streamlit`: For creating the web interface.
- `requests`: To fetch movie posters from The Movie Database (TMDb).
- `pickle`: For loading pre-saved movie data and similarity matrix.
- `pandas`: For data manipulation (used during preprocessing and model building).
- `scikit-learn`: For computing the cosine similarity.

You can install the dependencies using pip:

```bash
pip install streamlit requests pandas scikit-learn
```

## Usage

1. **Download/Prepare the Data Files**:  
   Make sure you have the `movie_list.pkl` and `similarity.pkl` files saved in the same directory as the script. These files contain the movie data and the precomputed similarity matrix.

2. **Run the Application**:
   Run the following command to start the Streamlit app:

   ```bash
   streamlit run app.py
   ```

   Once the app is running, you will be able to select a movie from the dropdown and view the 5 most similar movie recommendations with posters.

3. **Interact with the System**:  
   After selecting a movie, click the **'Show Recommendation'** button to view the suggested movies.

## Model Building and Preprocessing (`movie_recommender.ipynb`)

For those interested in understanding how the recommender system was built, the **`movie_recommender.ipynb`** file contains the following:

- **Data Preprocessing**: Steps to clean and prepare the movie data, including handling missing values, extracting relevant features, and transforming the data.
- **Model Building**: The implementation of the content-based recommender model, including the calculation of **Cosine Similarity** between movies based on their features such as genres, descriptions, etc.
- **Saving the Model**: The process of generating the similarity matrix and saving it as a pickle file (`similarity.pkl`), along with the movie list (`movie_list.pkl`).

### To use the notebook:
1. Open the `movie_recommender.ipynb` file in Jupyter Notebook or any other compatible environment.
2. Run each cell sequentially to understand the preprocessing and model-building steps.
3. The notebook will guide you through the entire process of creating the recommender model, from loading the data to generating the necessary files (`movie_list.pkl` and `similarity.pkl`).

## API

The system uses the TMDb API to fetch movie posters. You will need an API key from [The Movie Database](https://www.themoviedb.org/) to get the posters. Replace the placeholder API key in the `fetch_poster` function with your own.

## Example

- If you select the movie **"The Dark Knight"**, the system will recommend 5 movies that are most similar in content, such as **"Inception"**, **"Interstellar"**, and others, along with their posters.

## Project Structure

Here’s an overview of the project files:

- `app.py`: Main script for running the Streamlit application (for recommendations).
- `movie_recommender.ipynb`: Jupyter notebook containing the preprocessing and model-building code.
- `movie_list.pkl`: Pickled file containing the movie data (movie titles, IDs, etc.).
- `similarity.pkl`: Pickled file containing the precomputed similarity matrix for the movies.
- `README.md`: This file, which explains the project and how to run it.

## Conclusion

This content-based recommender system provides a simple yet effective way to suggest similar movies based on user input, utilizing cosine similarity to assess the closeness between movie features. It can be enhanced further with more sophisticated algorithms and additional movie features.

Happy watching! 🎬

