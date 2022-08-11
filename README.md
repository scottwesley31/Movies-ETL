# Movies-ETL
Module 8

## Project Description
Amazing Prime, which is a platform where movies and shows can be streamed online has developed a event for users called "The Hackathon". This event allows for users to predict the popularity of movies that are part of a clean dataset. The dataset for this event needs to be created first and involves the extraction of movie data from both Wikipedia and the MovieLens website. Data from these websites is merged into a single dataset and then loaded into a SQL database. The purpose of this project is to streamline the process by creating an automated pipeline which accomplishes this process utilizing less code overall. The code will transform the both the Wikipedia and MovieLens extracted data and then load two tables into SQL automatically (a table containing the movies with associated information and another table for rating information).

## Summary
4 separate Jupyter Notebook files were created:
1) ETL_function_test
2) ETL_clean_wiki_movies
3) ETL_clean_kaggle_data
4) ETL_create_database

### ETL_function_test
This file tests a function called `extract_transform_load()` which reads kaggle metadata, a MovieLens ratings CSV, and a Wikipedia data JSON file and transforms each of these into a Pandas DataFrame. The head of each DataFrame is displayed at the end of this file.

### ETL_clean_wiki_movies
This file incorporates a function called `clean_movie()` prior to the `extract_transform_load()` function which cleans the Wikipedia movie data from the JSON file by merging columns together with redundant data and changing the column names. The `extract_transform_load()` function now includes function within it called `parse_dollars()` which cleans up the data in the `Box office` column and `Budget` column. Regex is utilized to transform the `Box office`, `Budget`, `release_date`, and `Running time` columns each to a specific and uniform data format.

