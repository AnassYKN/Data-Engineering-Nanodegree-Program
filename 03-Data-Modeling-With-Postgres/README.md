# Project 1 Data Modeling Postgres

the goal of this project is to import the data that we recieve as JSON files to postgres DB by using modeling techniques.



## hierarchy of the workplace

- test.ipynb displays the first few rows of each table to let you check your database.
- create_tables.py drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts.
- etl.ipynb reads and processes a single file from song_data and log_data and loads the data into your tables. This notebook contains detailed instructions on the ETL process for each of the tables.
- etl.py reads and processes files from song_data and log_data and loads them into your tables. You can fill this out based on your work in the ETL notebook.
- sql_queries.py contains all your sql queries, and is imported into the last three files above.

## Schemas

### Fact Tables

songplays - records in log data associated with song plays i.e. records with page

+ songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

### Dimension Tables

users - users in the app

+ user_id, first_name, last_name, gender, level

songs - songs in music database

+ song_id, title, artist_id, year, duration

artists - artists in music database

+ artist_id, name, location, latitude, longitude

time - timestamps of records in songplays broken down into specific units

+ start_time, hour, day, week, month, year, weekday

## Build Etl Process

- Remember to run to reset tables.
```
$ python3 create_tables.py
```
```
$ python3 etl.py
```