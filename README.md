# mist4610project1
## group 8
## crn61608 


# Team Members:
1. Peng, Kimberly @[KimmyPenguin](https://github.com/KimmyPenguin)
2. Sivakumar, Srujana @[sruj-siva](https://github.com/sruj-siva)
4. Asgari, Neema @[Neemajoon](https://github.com/Neemajoon)
5. Modi, Maleeka @[m-modi](https://github.com/m-modi)
6. Palacherla, Asha @[ashapalacherla](https://github.com/ashapalacherla)

# Problem Description:
We chose this scenario because Spotify is one of the most popular music streaming services, with millions of users worldwide. The data model will allow us to better understand how various entities like songs, albums, and artists are interconnected in the system, which is highly relevant to both businesses in the music industry and tech professionals developing similar systems. With real-world applications, the model could be extended to track metrics like streams, monthly listeners, or the popularity of songs. This could serve as the foundation for building recommendation algorithms, analyzing user engagement, or making data-driven business decisions, which is crucial for the development of platforms similar to Spotify.


# Data Model: 
This database schema represents a structured design for a music streaming platform similar to Spotify. At its core, the artist table stores information about musicians, including their first and last names, biography, gender, and monthly listeners. Each artist is associated with a discography, which tracks their body of work and is linked through the discography_discography_id foreign key. 

The album table captures details about albums, including the title, release date, and references to both the artist and their discography. Each album contains multiple songs, stored in the song table, which records song titles, durations, genres, release dates, and the number of streams. Songs are linked to albums through album_album_id.


To track collaborations, the artist_has_song table establishes a many-to-many relationship between artists and songs, allowing for multiple artists on a single track. Similarly, playlists are managed through the playlist table, which includes details like title, save count, and creation date. The playlist_has_song table connects songs to playlists, enabling users to add multiple tracks to a playlist. Additionally, the playlist_has_artist table associates playlists with artists, making it possible to create artist-centric playlists. Overall, this schema efficiently structures relationships between artists, albums, songs, and playlists, facilitating seamless querying and management of music data in a SQL-based streaming platform.


# ERM Diagram:
![Image 3-13-25 at 2 43 PM](https://github.com/user-attachments/assets/c6f304c5-1533-473a-b55e-c73fd149ae54)

# Data Dictionaries

## Data Dictionary: Album
![Image 3-13-25 at 2 45 PM](https://github.com/user-attachments/assets/3987cdef-b566-4d22-a196-764e12408701)

## Data Dictionary: Song
![Image 3-13-25 at 2 46 PM](https://github.com/user-attachments/assets/6e400a94-36d5-4dc5-ab2f-75e9baa31752)

## Data Dictionary: Playlist
![Image 3-13-25 at 2 47 PM](https://github.com/user-attachments/assets/a3eb7f67-8abf-484d-93ef-892da39a4dd9)

## Data Dictionary: Discography
![Image 3-13-25 at 2 47 PM (1)](https://github.com/user-attachments/assets/b55f7923-02ef-4b19-8442-60b55d6ecd1c)

# Data Dictionary: artist has song
![Image 3-13-25 at 2 48 PM](https://github.com/user-attachments/assets/bf6247a1-221a-4cac-acc2-3e6912c29393)

## Data Dictionary: playlist has song
![Image 3-13-25 at 2 48 PM (1)](https://github.com/user-attachments/assets/0e82496f-d1a2-46a0-9319-f9c61ac4edc2)

## Data Dictonary: playlist has artist
![Image 3-13-25 at 2 53 PM](https://github.com/user-attachments/assets/def45731-e768-45f4-a095-c3f93561b47c)

# Queries:

## Complex Queries

1. Find the top three songs in the pop genre

![image](https://github.com/user-attachments/assets/2c6b8e7b-225b-424f-8eda-49498e6bcede)

This information helps us determine which pop songs are currently the most streamed and can even compare them to past trends. We can also identify audience preferences and common elements among the top pop songs, providing valuable insights into what drives their popularity.

2. Find artists that are in popular playlists & count how many they appear in

![image](https://github.com/user-attachments/assets/2d968860-bf45-435f-a3d9-34b3aebd93da)

Knowing how many playlists an artist appears in, as well as which playlists have the most amount of likes and listens is a great way to separate artists that appeal to listeners outside a specific genre, and general songs that a wide variety of users like to listen to regardless of their normal taste in music. Being able to find outliers like these is helpful to see what artists are able to reach listeners outside of their usual bubble.

3. Total streams of each genre in descending order

![image](https://github.com/user-attachments/assets/df22b2aa-c4d1-4884-a376-1ba7f0dcd71c)

This is important for a manager to know so that we can see which songs are popular within the genre versus the songs that have made waves outside of the genre and have reached a wider population and has accumulated some merit from a greater  audience than what the genre normally sees.

4. Show all artists with the number of albums they released

![image](https://github.com/user-attachments/assets/1d28f5b4-3337-49b3-be8b-b1a5e462827e)

 This is important to managers because of how important general artist stats are. Knowing how many albums (and subsequently, songs) an artist has released is important because this helps to see how much music an artist has made by any given time, which helps when considering streams and monthly listens.

5. Find out if song exists in artists discography

![image](https://github.com/user-attachments/assets/f8d70f73-d47a-45f9-a5d8-8b29486d5418)

This is important to managers because so many songs have been released throughout time and knowing if a song stuck in a users head is by a specific singer they might know, or if someone recommended a song but the user forgot the artists name, this search input lets them know that whichever artist they searched in has a released song by that name.

6. Shows how many albums released by an artist each year

![image](https://github.com/user-attachments/assets/79ac676f-f812-4918-a36c-72efa7168790)

 This is important for managers to know in order to benchmark yearly releases and streams to be able see how many albums have been released in descending order by year, allowing us to get a full understanding of how many songs and albums and pacing of album releases various artists have had compared to other artists.
 

## Simple Queries

1. List top artist in each genre

![image](https://github.com/user-attachments/assets/37f6cd7d-bfe1-4d3a-9e08-813feb2f75d7)

This is important to managers because this allows them to see who is currently at the top of the music game. This can give insights on how well a manager’s own artists are doing, as well as the competition. This can also be used to scope out potential musicians to collaborate with that can help increase the manager’s own artists popularity.

2. Find a Song that was played less/more than X number of times with that artist information

![image](https://github.com/user-attachments/assets/291df28c-f8c4-414c-8261-fcd4c6587d10)

Allows us to filter through songs the general population really likes, or really dislikes. By filtering every song by the number of streams it has, we are able to gain insights on what the general population likes to listen to, what the most and least streamed songs are, see basic artist and album information

3. Finding out the most streamed songs

![image](https://github.com/user-attachments/assets/f36d45ef-f915-4a58-8f8d-24168fe1b1a6)

With this query, we gain insights into the popularity of a specific artist or song, uncover the key elements that contribute to a song's success, and identify patterns in music consumption. Additionally, we can analyze how factors such as genre, release date, and duration influence a song’s performance.

4.  Report all songs in the ‘pop’ category that have been added to any playlist
   
![image](https://github.com/user-attachments/assets/16c0eba3-1afc-415c-8b3e-d0717846b4ce)

This is important to managers because we can see (by genre specifically) that suits the most number of people’s music taste. This helps with choosing top songs of any given genre, as well as makes it easier to curate genre-based playlists and Spotify Wrapped profiles to users who tend to stick to one genre/heavily prefer one genre over others.


# Database information:
## Name of the database: ha_group8
![image](https://github.com/user-attachments/assets/6e7a009f-f37b-40ea-ab0f-986ef928b749)

