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

![image](https://user-images.githubusercontent.com/94148420/154396076-81c272e6-0d39-4f40-9277-48fb7b5526d0.png)

**kaggle_metadata Output**

![image](https://user-images.githubusercontent.com/94148420/154396216-36e64987-099a-4a0e-9c1d-7d5183831e8d.png)

**ratings DataFrame Output**

![image](https://user-images.githubusercontent.com/94148420/154396735-b61c89c9-645b-46f4-a052-6c0f42011d1f.png)

### Extract and Transform the Wikipedia Data

The next step was to extract and transform the Wikipedia data so that it could be merged with the Kaggle data.

**wiki_movies_df DataFrame Output**

![image](https://user-images.githubusercontent.com/94148420/154397821-c57c6edb-9e33-4d6b-b590-725b3922b2dd.png)

**wiki_movies_df.columns.to_list() Output**

![image](https://user-images.githubusercontent.com/94148420/154397934-4f11d937-1422-4b7b-a4e1-a6298c88d3ff.png)

### Extract and Transform the Kaggle Data

The ultimate output of this step is to merge the MovieLens rating DataFrame wiht the movies_df DataFrame to create the movies_with_ratings_df.

**movies_with_ratings_df.head() Output**

![image](https://user-images.githubusercontent.com/94148420/154398472-54b5eb9d-21f1-408c-a8e9-026ffdc64ddd.png)

**movies_df.head() Output**

![image](https://user-images.githubusercontent.com/94148420/154398589-6b0de1c5-3614-4b1c-b259-28ee54c1250b.png)

### Create the Movie Database

The final step was to movies_df DataFrame MovieLens ratings CSV file to a SQL database.

The movies table has 6052 rows:

![image](https://user-images.githubusercontent.com/94148420/154398931-733f6077-3f1a-4e40-8196-dc2f4514c989.png)

The ratings table has 26,024,289 rows:

![image](https://user-images.githubusercontent.com/94148420/154399048-b1b3b8a7-7ed4-4760-bf3e-0293d47ea484.png)


## Summary

This was a very challenging project, but the final outcome for Amazing Prime was accomplished.  Three files were extracted, transformed, then ulitmately loaded into a SQL database.  The most challenging of these steps was the transformation of the data, where there was much thought put into the "cleaning" of the data.
