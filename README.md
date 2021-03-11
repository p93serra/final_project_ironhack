![Ironhack logo](https://i.imgur.com/1QgrNNw.png)

# Ironhack | Final Project | How to make popular songs using Machine Learning?

In this project we would create a predictor of popularity of the Songs in Spotify and we create a lyrics generator trained with lyrics of two artists. In order to get the lyrics we have created a lyrics extractor that uses the APIs of Spotify and Genius. The main objective of this project is to explore the capabilities of Machine Learning to create good music.

## Content 📋

Folder structure:
- _data_: contains the databases used and generated during this project:
    - _kaggle_data.csv_: database with +170k songs downloaded from Kaggle.
    - _songs_ed_sheeran_elton_john.csv_: example of dataframe of all songs after lyrics extraction.
    - _songs_sheeran_john_cleaned.csv_: example of dataframe of all songs after lyrics cleaning.
    - _sheeran_john_lyrics.txt_: example of text file with all lyrics after lyrics complilator.
- _models_: contains the two models generated during this project: _lyrics generator_ and _popularity predictor_
- _code_: contains the python files used to download the songs from spotify:
    - _song_database_generator.py_
- _notebooks_: contains the different notebooks used:
    - _data_cleaning.ipynb_: notebook to clean the lyrics.
    - _data_modeling.ipynb_: notebook used to generate the model to predict _popularity.
    - _lyrics_compilator.ipynb_: notebook used to compile all cleaned lyrics in one file.
    - _lyrics_generator.ipynb_: notebook used to generate the lyrics generator.
    - _song_lyrics_extractor.ipynb_: notebook used to download the lyrics from Genius.

## Libraries used 🔧

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install the different libraries for this project.

```bash
# Library to communicate with Spotify API.
pip install spotipy
# Library to communicate with Genius API.
pip install lyricsgenius
# Library to detect language of lyrics.
pip install langdetect
# Library to correct spelling errors.
pip install autocorrect
# Library to make sentiment analysis.
pip install textblob
```

## Usage 🛠️

To complete the Lyrics Generator project you should follow this sequence:

1) Generate the Songs Database:

```bash
python3 /code/song_database_generator.py
```

```python
>>> URL of the playlist to append: https://open.spotify.com/playlist/0FDfSMiFQ16YF0uXh3UBPG?si=h_UXIwYKS7mavj-rDoK6dw
Finished!
Processed: 0/3
Processed: 3/3
Previous database len: 505
New database len: 508
```

2) Extract lyrics:
Open notebook _song_lyrics_extractor.ipynb_ and execute the full notebook changing the path of the Songs Database:

```python
main("../data/songs_lyrics_complete.csv")
```

3) Lyrics Cleaning:
Open notebook _data_cleaning.ipynb_ and execute the full notebook changing the path of the Lyrics Database:

```python
df = pd.read_csv("../data/songs_ed_sheeran_elton_john.csv")
```

4) Lyrics Compilator:
Open notebook _lyrics_compilator.ipynb_ and execute the full notebook changing the path of the Cleaned Lyrics Database:

```python
songs_clean = pd.read_csv('../data/songs_sheeran_john_cleaned.csv')
```

5) Lyrics Generator:
Open notebook _lyrics_generator.ipynb_ and execute the full notebook changing the path of the Cleaned Lyrics text file:

```python
f = open("sheeran_john_lyrics.txt", "r")
```

## Authors ✒️

Pau Serra - pau.serra.bergeron@gmail.com

## Licence 📄

Free to used it but:
* Share this project if you appreciate it 📢
* You can buy a 🍺 or ☕ to the team.
* Share your improvements or errors spotted 🤓
* etc.
