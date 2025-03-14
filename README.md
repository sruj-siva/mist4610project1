# mist4610project1
# group 8
# crn61608 


Team Members:
1. Peng, Kimberly @KimmyPenguin(https://github.com/KimmyPenguin)
2. Sivakumar, Srujana @sruj-siva(https://github.com/sruj-siva)
4. Asgari, Neema @Nemmajoon(https://github.com/Nemmajoon)
5. Modi, Maleeka @m-modi(https://github.com/m-modi)
6. Palacherla, Asha @ashapalacherla(https://github.com/ashapalacherla)

Problem Description:

We chose this scenario because Spotify is one of the most popular music streaming services, with millions of users worldwide. The data model will allow us to better understand how various entities like songs, albums, and artists are interconnected in the system, which is highly relevant to both businesses in the music industry and tech professionals developing similar systems. With real-world applications, the model could be extended to track metrics like streams, monthly listeners, or the popularity of songs. This could serve as the foundation for building recommendation algorithms, analyzing user engagement, or making data-driven business decisions, which is crucial for the development of platforms similar to Spotify.


Data Model: 
This database schema represents a structured design for a music streaming platform similar to Spotify. At its core, the artist table stores information about musicians, including their first and last names, biography, gender, and monthly listeners. Each artist is associated with a discography, which tracks their body of work and is linked through the discography_discography_id foreign key. 

The album table captures details about albums, including the title, release date, and references to both the artist and their discography. Each album contains multiple songs, stored in the song table, which records song titles, durations, genres, release dates, and the number of streams. Songs are linked to albums through album_album_id.


To track collaborations, the artist_has_song table establishes a many-to-many relationship between artists and songs, allowing for multiple artists on a single track. Similarly, playlists are managed through the playlist table, which includes details like title, save count, and creation date. The playlist_has_song table connects songs to playlists, enabling users to add multiple tracks to a playlist. Additionally, the playlist_has_artist table associates playlists with artists, making it possible to create artist-centric playlists. Overall, this schema efficiently structures relationships between artists, albums, songs, and playlists, facilitating seamless querying and management of music data in a SQL-based streaming platform.


ERM Diagram:
![Image 3-13-25 at 2 43 PM](https://github.com/user-attachments/assets/c6f304c5-1533-473a-b55e-c73fd149ae54)

Data Dictionary: Album
![Image 3-13-25 at 2 45 PM](https://github.com/user-attachments/assets/3987cdef-b566-4d22-a196-764e12408701)

Data Dictionary: Song
![Image 3-13-25 at 2 46 PM](https://github.com/user-attachments/assets/6e400a94-36d5-4dc5-ab2f-75e9baa31752)

Data Dictionary: Playlist
![Image 3-13-25 at 2 47 PM](https://github.com/user-attachments/assets/a3eb7f67-8abf-484d-93ef-892da39a4dd9)

Data Dictionary: Discography
![Image 3-13-25 at 2 47 PM (1)](https://github.com/user-attachments/assets/b55f7923-02ef-4b19-8442-60b55d6ecd1c)

Data Dictionary: artist has song
![Image 3-13-25 at 2 48 PM](https://github.com/user-attachments/assets/bf6247a1-221a-4cac-acc2-3e6912c29393)

Data Dictionary: playlist has song
![Image 3-13-25 at 2 48 PM (1)](https://github.com/user-attachments/assets/0e82496f-d1a2-46a0-9319-f9c61ac4edc2)

Data Dictonary: playlist has artist
![Image 3-13-25 at 2 53 PM](https://github.com/user-attachments/assets/def45731-e768-45f4-a095-c3f93561b47c)

Queries: 
