# Movie Recommendation System

This Movie Recommendation System suggests the top 5 movies similar to a given movie. The system uses cosine similarity to find the most similar movies based on genres, cast, and other attributes. A Streamlit-based user interface is provided for a seamless and interactive experience.

## Features

- **Streamlit UI**: An interactive web app for users to input a movie title and receive recommendations.
- **Content-Based Filtering with Cosine Similarity**: Recommends movies similar in attributes such as genre, cast, and crew.
- **Top 5 Recommendations**: The system outputs the top 5 most similar movies based on cosine similarity scores.
- **Model Loading**: A pre-trained recommendation model is stored in the `model` folder for quick startup.

## Dataset

This system is based on the [TMDB Movie Metadata dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata) from Kaggle, which includes movie details like:

- Title
- Genre
- Cast
- Crew
- Overview (summary)

### Downloading the Dataset

To download the dataset from Kaggle, use the following command:

```bash
kaggle datasets download -d tmdb/tmdb-movie-metadata
```

After downloading, unzip the dataset and place the CSV file in the project directory.

## Installation

1. **Clone the repository**:

    ```bash
    git clone https://github.com/yourusername/movie-recommender-system.git
    cd movie-recommender-system
    ```

2. **Install dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

3. **Kaggle API Setup**: If not already set up, configure the Kaggle API by placing your `kaggle.json` file in the correct directory.

4. **Download the dataset** and place the data file in the project folder if not already included.

## Usage

### Running the Streamlit App

To start the Streamlit app, use the following command:

```bash
streamlit run app.py
```

### Using the App

1. Open the app in your browser (usually opens automatically; otherwise, go to `http://localhost:8501`).
2. Enter the title of a movie in the search box.
3. Click "Get Recommendations" to see the top 5 recommended movies.

### Example Output

Upon entering a movie title (e.g., "Inception"), you should see an output similar to:

```
Recommended Movies:
1. Interstellar
2. The Matrix
3. Shutter Island
4. Minority Report
5. The Prestige
```

## Project Structure

- **app.py**: The main application file for the Streamlit UI.
- **model/**: Contains the pre-trained model for recommendations.
- **recommend.py**: Core recommendation logic, including cosine similarity calculations.
- **data/**: Contains the movie dataset (if not directly downloaded via Kaggle).

## Recommendation Methodology

This recommendation system uses **Cosine Similarity** to measure similarity between movies based on attributes such as genre, cast, and crew. Here’s a brief overview of the process:

1. **Data Preprocessing**: Vectorizes text-based movie attributes (e.g., genres, cast).
2. **Cosine Similarity**: Calculates cosine similarity scores between the input movie and all others in the dataset.
3. **Top Recommendations**: Outputs the top 5 most similar movies based on cosine similarity.

## Customization

- **Number of Recommendations**: The default is set to 5. You can adjust this number in the code.
- **Dataset Modifications**: The model can work with modified datasets as long as movie attributes (title, genre, etc.) are present.

## Dependencies

- Python 3.x
- Streamlit
- Pandas
- Numpy
- Scikit-learn
- NLTK
- Kaggle API (optional for dataset download)

## Contributing

Feel free to open issues or submit pull requests for any enhancements!

## License

This project is licensed under the MIT License.

---
