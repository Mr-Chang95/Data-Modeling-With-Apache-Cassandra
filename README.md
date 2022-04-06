#  Modeling with Apache Cassandra

## Project Description
This is a project done as part of the [Udacity Data Engineering Nanodegree program](https://www.udacity.com/course/data-engineer-nanodegree--nd027?utm_source=gsem_brand&utm_medium=ads_r&utm_campaign=12712700850_c&utm_term=124530975350&utm_keyword=udacity%20data%20engineering_e&gclid=CjwKCAjw0a-SBhBkEiwApljU0pc-sn1RkKZQdwySslc8H1ncIw8LiEBscBNhqx3vKCBTTOdq7rxsZBoCBf0QAvD_BwE).A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

They'd like a data engineer to create an Apache Cassandra database which can create queries on song play data to answer the questions, and wish to bring you on the project.  To complete the project, I will model the data by creating tables in Apache Cassandra to run queries. Then, I will complete an ETL pipeline that transfers data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables.

## Dataset
There is only one dataset named `event_data` which is in a directory of CSV files partitioned by date. Here are two examples of filepaths to two files in the dataset:
> `event_data/2018-11-08-events.csv`

## Queries/Questions
For NoSQL databases, we design the schema based on the queries we know we want to perform. In other words, we are modeling our schema after our questions. For this project, these are the 3 questions/queries we are interested in finding the answers to:

1. Find artist, song title and song length that was heard during `sessionId`=338, and `itemInSession`=4.
    - `SELECT artist, song, length from table_1 WHERE sessionId=338 AND itemInSession=4`
2. Find name of artist, song (sorted by `itemInSession`) and user (first and last name) for `userid`=10 and `sessionId`=182.
    - `SELECT artist, song, firstName, lastName FROM table_2 WHERE userId=10 and sessionId=182`
3. Find every user name (first and last) who listened to the `song` 'All Hands Against His Own'.
    - `SELECT firstName, lastName WHERE song='All Hands Againgst His Own'`

## Instructions
Run each portion of `Project_1B_Project_Template.ipynb` to create the tables and build the ETL pipeline.

## ETL Pipeline
1. Start with the raw csv data files as described in dataset.
2. For each row of the csv data, insert the data in the appropriate column.
3. Perform the Select queries to answer the questions.
