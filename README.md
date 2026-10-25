# 🎵 Spotify Song Recommender

A Streamlit app that predicts a song's genre from audio features you choose, then recommends the closest matching tracks in that genre.

**Author:** Raahima Rashid Peracha, BS Data Science (3A)
**Course:** Artificial Intelligence (Lab), Instructor: Sir Rasikh Ali

## How it works
1. Set your preferences (popularity, energy, danceability, valence, tempo, etc.) in the sidebar.
2. A **Decision Tree classifier** (`max_depth=10`) predicts the genre from 15 audio features.
3. **Cosine similarity** ranks songs within that genre and returns your top N matches.

## Dataset
[Spotify Tracks Dataset (Kaggle)](https://www.kaggle.com/datasets/saichaitanyareddyai/spotify-tracks-dataset-audio-features/data): 114,000 tracks, 114 genres. The model is trained on the 20 largest genres (20,000 tracks, 70/30 train-test split), with about 45% accuracy.

## Project files
| File | Description |
|---|---|
| `app.py` | Streamlit web app |
| `task_project.ipynb` | Data cleaning, training and evaluation |
| `spotify.pkl` | Trained Decision Tree model |
| `spotify-tracks-dataset-detailed.csv` | Dataset |

## Run locally
```bash
pip install streamlit pandas numpy scikit-learn joblib
streamlit run app.py
```
Keep `spotify.pkl` and the CSV in the same folder as `app.py`.

## Tech stack
Python, Pandas, NumPy, scikit-learn, Streamlit, Joblib
