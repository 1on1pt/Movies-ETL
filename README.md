# Movies-ETL

## Overview of the Project
Amazing Prime loves the original dataset that was created and Britta needs assistance in developing an automated pipeline that will extract new data, transform this data, then load into existing tables.  This was accomplished by refactoring the original code to create one function that will take in the Wikipedia data, the Kaggle metadata, and the MovieLens rating data, perform the extract, transform, and load (ETL) process, the import to a PostgreSQL database.

### Resources

Data Source:
     * wikipedia-movies.json
     * movies_metadata.csv; ratings.csv

Code: 
     * ETL_function_test.ipynb
     * ETL_clean_wiki_movies.ipynb
     * ETL_clean_kaggle_data.ipynb
     * ETL_create_database.ipynb

Software: 
     * Python 3.7.6
     * Pandas 1.3.5
     * Jupyter Notebook
     * pgAdmin 6.1

## Creating an Automated Pipeline

The following is the pathway that created the automated pipeline for Amazing Prime.

### Write an ETL Function to Read Three Data Files

The first step in this process was to write an ETL function that would read the three data files.  The output would be the wiki_movies_df DataFrame, the kaggle_metadata DataFrame, and the ratings DataFrame.

**wiki_movies_df DataFrame Output**



### Extract and Transform the Wikipedia Data



### Extract and Transform the Kaggle Data



### Create the Movie Database


## Summary


