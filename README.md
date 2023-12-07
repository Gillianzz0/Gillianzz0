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

**1. View the Top 10 Songs of a Specific Year**

```python
# Filter songs for the year 1988 and display the top 10 songs
songs_specific_year = songs_df[songs_df['year'] == 1988].sort_values(by='rank', ascending=True)
print(songs_specific_year.head(10))

**Question:** Which were the top 20 songs in the year 1980?

**Question:** Who are the top 20 artists with the most songs in the dataset?

```python
# Count the number of songs per artist and select the top 20
artist_counts = songs_df['artist'].value_counts().head(20)
# Create a bar plot to visualize the top 20 artists with the most songs
artist_counts.plot(kind='bar', figsize=(14, 7), color='skyblue', edgecolor='black', title='Top 20 Artists with the Most Songs in the Dataset')

