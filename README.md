# Music Database SQL Project

This project was completed as part of graduate coursework in Business Analytics and AI at Northern Illinois University. It involves designing and querying a relational database to model a music streaming and event ecosystem.

## Overview
- Designed a relational database schema for artists, albums, songs, playlists, users, and events  
- Created normalized tables with primary and foreign key relationships  
- Implemented the database in Snowflake using SQL  
- Wrote queries to extract meaningful insights across multiple related tables  

## Database Design
- Built a normalized schema with multiple entity relationships  
- Implemented junction tables to handle many-to-many relationships (e.g., playlists, events, albums)  
- Ensured referential integrity using primary and foreign keys  

The ERD diagram included in this repository illustrates the relationships between entities such as Artist, Album, Song, Playlist, Event, and User.

## SQL Techniques Used
- Table creation and data insertion  
- Joins (INNER, LEFT, RIGHT)  
- Filtering and conditional queries  
- Aggregation and sorting  
- Multi-table joins across relational structures  

## Example Queries
- Identified events by location (e.g., California, Chicago, Milwaukee)  
- Retrieved artists performing at specific events  
- Analyzed playlist compositions and associated songs  
- Queried user and subscription data tied to playlists  
- Joined multiple tables to connect artists, albums, and songs

## Example Query

```sql
SELECT artist_name, s.song_title, s.song_genre
FROM artist a
JOIN artist_albums aa ON a.artist_id = aa.artist_id
JOIN album_songs als ON aa.album_id = als.album_id
JOIN song s ON als.song_id = s.song_id
WHERE s.song_genre = 'Toddler';
```

## Files in this Repository
- SQL table creation and data insertion scripts  
- SQL query scripts  
- ERD diagram showing database relationships  

## Outcome
This project demonstrates the ability to design relational databases, implement them in SQL, and write complex queries to extract insights from structured data.
