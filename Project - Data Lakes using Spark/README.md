# Project Overview #

A music streaming startup, Sparkify, has grown their user base and song database even more and want to move their data warehouse to a data lake. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

# Project Description #

Build an ETL pipeline that extracts their data from S3, processes them using Spark, and loads the data back into S3 as a set of dimensional tables. This will allow their analytics team to continue finding insights in what songs their users are listening to.

# Database schema #

## Fact Table ##

1. songplays - records in log data associated with song plays i.e. records with page NextSong
* songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

## Dimension Tables ##

1. users - users in the app
* user_id, first_name, last_name, gender, level
2. songs - songs in music database
* song_id, title, artist_id, year, duration
3. artists - artists in music database
* artist_id, name, location, lattitude, longitude
4. time - timestamps of records in songplays broken down into specific units
* start_time, hour, day, week, month, year, weekday

# Project files #

The project includes 3 files:

1. dl.cfg: Contains AWS credentials
2. etl.py: Reads data from S3, processes data using Spark and writes them back to S3.
3. README.md: Provides discussions and overview of the project.