# Top US Songs from 1950 to 2019 with Lyrics Dataset

## Dataset Description

This dataset includes details about popular songs in the United States from 1950 to 2019. It provides comprehensive information on song rankings, lyrics, artists, and genres over several decades.

## Variables in the Dataset

| Variable | Description                              | Data Type   |
|----------|------------------------------------------|-------------|
| Rank     | The chart ranking of the song.           | Integer     |
| Song     | The title of the song.                   | String      |
| Artist   | The artist who performed the song.       | String      |
| Year     | The year the song was released.          | Integer     |
| Lyrics   | The lyrics of the song.                  | String      |
| Length   | The duration of the song.                | Time        |
| Genre    | The genre of the song.                   | String      |

## Potential Uses

This dataset can be used for analyzing trends in music, lyrical themes, and the evolution of different music genres over time.

## Creator and Source

- **Dataset Creator**: Stefan Comanita
- **Source**: [Kaggle Dataset](https://www.kaggle.com/datasets/stefancomanita/top-us-songs-from-1950-to-2019-w-lyrics)

## Data Analysis and Visualization

### 1. View the Top 10 Songs of a Specific Year

```python
songs_specific_year = songs_df[songs_df['year'] == 1988].sort_values(by='rank', ascending=True)
print(songs_specific_year.head(10))

### 2. Explore the Top 20 Songs of the Year 1980

**Question:** Which were the top 20 songs in the year 1980?

```python
songs_1980 = songs_df[songs_df['year'] == 1980].sort_values(by='rank', ascending=True)
print(songs_1980.head(20))

### 3. Analyze the Top 20 Artists with the Most Songs

**Question:** Who are the top 20 artists with the most songs in the dataset?

```python
artist_counts = songs_df['artist'].value_counts().head(20)
artist_counts.plot(kind='bar', figsize=(14, 7), color='skyblue', edgecolor='black', title='Top 20 Artists with the Most Songs in the Dataset')
