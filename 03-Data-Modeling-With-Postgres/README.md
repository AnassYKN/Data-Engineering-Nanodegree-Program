Files used on the project:

	data folder nested at the home of the project, where all needed jsons reside.
	sql_queries.py contains all your sql queries, and is imported into the files bellow.
	create_tables.py drops and creates tables. You run this file to reset your tables before each time you run your ETL scripts.
	test.ipynb displays the first few rows of each table to let you check your database.
	etl.ipynb reads and processes a single file from song_data and log_data and loads the data into your tables.
	etl.py reads and processes files from song_data and log_data and loads them into your tables.
	current file, provides discussion on my project.

1.Fact Table:

-songplays - records in log data associated with song plays i.e. records with page NextSong

songplay_id (INT) PRIMARY KEY: ID of each user song play
start_time (DATE) NOT NULL: Timestamp of beggining of user activity
user_id (INT) NOT NULL: ID of user
level (TEXT): User level {free | paid}
song_id (TEXT) NOT NULL: ID of Song played
artist_id (TEXT) NOT NULL: ID of Artist of the song played
session_id (INT): ID of the user Session
location (TEXT): User location
user_agent (TEXT): Agent used by user to access Sparkify platform

2.Dimension Tables:

-users - users in the app

user_id (INT) PRIMARY KEY: ID of user
first_name (TEXT) NOT NULL: Name of user
last_name (TEXT) NOT NULL: Last Name of user
gender (TEXT): Gender of user {M | F}
level (TEXT): User level {free | paid}

-songs - songs in music database

song_id (TEXT) PRIMARY KEY: ID of Song
title (TEXT) NOT NULL: Title of Song
artist_id (TEXT) NOT NULL: ID of song Artist
year (INT): Year of song release
duration (FLOAT) NOT NULL: Song duration in milliseconds

-artists - artists in music database

artist_id (TEXT) PRIMARY KEY: ID of Artist
name (TEXT) NOT NULL: Name of Artist
location (TEXT): Name of Artist city
lattitude (FLOAT): Lattitude location of artist
longitude (FLOAT): Longitude location of artist

-time - timestamps of records in songplays broken down into specific units

start_time (DATE) PRIMARY KEY: Timestamp of row
hour (INT): Hour associated to start_time
day (INT): Day associated to start_time
week (INT): Week of year associated to start_time
month (INT): Month associated to start_time
year (INT): Year associated to start_time
weekday (TEXT): Name of week day associated to start_time