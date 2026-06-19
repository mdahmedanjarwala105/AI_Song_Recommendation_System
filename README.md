# AI Song Recommendation System

A content-based song recommendation system using TF-IDF vectorization and cosine similarity to suggest similar songs based on metadata features.

## Features

- Content-based filtering using song metadata (genre, artist, title features)
- TF-IDF vectorization for text feature extraction from genre and metadata
- Cosine similarity computation for song matching
- Song recommendation engine with customizable output
- Sample dataset of 50 songs across 30+ genres for demonstration

## Dataset

The repository includes `sample_songs_csv.csv` containing 50 songs with metadata including:
- song_id, title, artist, genre
- duration_ms, popularity, release_year

Genres span Pop, Rock, Jazz, Electronic, Country, Ambient, Metal, R&B, Folk, Dubstep, Indie, Classical, Reggae, Hip Hop, Blues, Techno, Punk, World, Lo-fi, Gospel, Salsa, Alternative, Disco, Trap, Indie Rock, Soul, New Wave, Grunge, Synthpop, Bossa Nova, Progressive Rock, Minimalist, Experimental, Pop Punk, Funk, Singer-Songwriter, Death Metal, Dream Pop, Bluegrass, Trance, Ska, Post Rock, Garage Rock, Dark Ambient, Surf Rock, Math Rock, and Chillwave.

## Tech Stack

- **Python** - Core programming language
- **scikit-learn** - TF-IDF vectorization and cosine similarity
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computations

## Project Structure

```
AI_Song_Recommendation_System/
├── notebook/
│   └── AI_Recommendation_System.ipynb   # Main Jupyter notebook
├── sample_songs_csv.csv               # Sample song dataset (50 songs)
├── Pipfile                           # Pipenv dependencies
├── Pipfile.lock                      # Pipenv lock file
└── README.md                         # Project documentation
```

## Installation

### Using Pipenv

```bash
pip install pipenv
pipenv install
pipenv run jupyter notebook
```

### Using pip

```bash
pip install -r requirements.txt
```

## Usage

1. Open the notebook in the `notebook/` directory:
   ```bash
   jupyter notebook notebook/AI_Recommendation_System.ipynb
   ```
2. The system loads the song dataset from `sample_songs_csv.csv`
3. TF-IDF vectors are computed from the song metadata features
4. Cosine similarity is calculated between all song pairs
5. Provide a song title to get recommendations based on similarity scores

## How It Works

1. **Data Loading**: Songs are loaded from the CSV dataset into a pandas DataFrame
2. **Text Preprocessing**: Genre and other text features are cleaned and combined
3. **TF-IDF Vectorization**: Text features are converted to numerical vectors using Term Frequency-Inverse Document Frequency
4. **Cosine Similarity**: Pairwise similarity scores are computed between all songs
5. **Recommendation**: The system returns the top-N most similar songs for a given input song, excluding the input itself

## License

MIT License - see the [LICENSE](LICENSE) file for details.
