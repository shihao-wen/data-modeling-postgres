# Data Modeling with Postgres

## Project Introduction

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

They'd like a data engineer to create a Postgres database with tables designed to optimize queries on song play analysis, and bring you on the project. Your role is to create a database schema and ETL pipeline for this analysis. You'll be able to test your database and ETL pipeline by running queries given to you by the analytics team from Sparkify and compare your results with their expected results.

## Project Workflow

- Define fact and dimension tables (Star Schema) 

- Model data with Postgres and build ETL pipeline

## Dataset

### Song dataset

The first dataset is a subset of real data from the [Million Song Dataset](http://millionsongdataset.com/). Each file is in JSON format and contains metadata about a song and the artist of that song. The files are partitioned by the first three letters of each song's track ID.

### Log dataset

The second dataset consists of log files in JSON format generated by this [event simulator](https://github.com/Interana/eventsim) based on the songs in the dataset above. These simulate activity logs from a music streaming app based on specified configurations.

## File Description

    .
    ├── create_tables.py        # Create, & drop tables
    ├── etl.py                  # Read & process data into database tables
    ├── sql_quires.py           # Include all sql quries and import data into tables
    ├── etl.ipynb               # Read & process data into database tables
    ├── test.ipynb              # Check Postgres database and table validility
    └── README.md

test.ipnb displays the first few rows of each table to let you check your database

create_tables.py drops and created your table

etl.ipynb read and processes a single file from song_data and log_data and loads into your tables in Jupyter notebook

etl.ipynb read and processes a single file from song_data and log_data and loads into your tables in ET

sql_queries.py containg all your sql queries and in imported into the last three files above

### Instructions:

1. Run `python create_tables.py` to connect to the Sparkify database, drops any tables if they exist, and creates the tables.

2. Run `python etl.py` to connect to the Sparkify database, extracts and processes the log_data and song_data, and loads data into the five tables.

3. Run `test.ipynb` to check if table was created and etl pipline was ran successfully.
