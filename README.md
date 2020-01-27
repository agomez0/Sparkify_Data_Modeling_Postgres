# Sparkify Data Modeling with Postgres

Sparkify is a startup company that needs help structuring their data in a way that makes it easy to query; particularly to analyze the songs users are listening to on the music streaming app. The goal here is to create a star-schema database using Postgres to efficiently store the data. An ETL pipeline is created to transfer metadata from JSON logs into tables.

## Files:
* `data`: contains JSON metada.
* `sql_queries.py`: DROP, CREATE, and INSERT statements to create tables.
* `etl.ipnyb`: loads a single file of data into tables.
* `etl.py`: loads all files of data into tables.
* `test.ipynb`: preview the first few rows of tables.

## Schema:
Fact Table
    1. songplays: records in log data associated with song plays (records with page "NextSong")
        - songplay_id
        - start_time
        - user_id
        - level
        - song_id
        - artist_id
        - session_id
        - location
        - user_agent

Dimension Tables
    2. users: app users
        - user_id
        - first_name
        - last_name
        - gender
        - level
    3. songs: songs in music database
        - song_id
        - title
        - artist_id
        - year
        - duration
    4. artists: artists in music database
        - artist_id
        - name
        - location 
        - latitude
        - longitude
    5. time: timestamps of records in songplays broken into specific units
        - start_time
        - hour
        - day
        - week
        - month
        - year
        - weekday






