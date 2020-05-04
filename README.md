# Movies-ETL
Movies-ETL
Extract, Transform and Load (ETL) from Wikipedia(JSON format), Kaggle(csv file) MovieLens_Ratings (csv file) into PostgreSQL, perform the transfromation step by python and pandas.

Resources:
a unstructure web-scraped JSON file of over 5,000 movies from 1990 to 2019, from wikipediawikipedia.movies.json

a unstructure csv file from Kaggle movies_metadata.csv

a large unstructure csv file from MovieLens with movie rating information (ratings.csv)

Outputs:

ETL Jupyter NoteBooks movies_ETL.ipynb

# Challenge

Goals:
Create an automated ETL pipeline.

Extract data from multiple sources.

Clean and transform the data automatically using Pandas and regular expressions.

Load new data into existing tables in PostgreSQL

Challenge Outputs:

Challenge automated Pipeline Jupyter NoteBooks challenge.ipynb

## Assumptions

Assumption 1:Input data resources are keeping same formats, same columns name, 
                same column's order and same data types.
                
Assumption 2: wiki_data has same alternate titles

Assumption 3: wiki_data: 'Box_office', 'Budget','release date' and 'running_time 'columns 
                have consistent data types and format followed by assumed Regex rules
                
Assumption 4: kaggle_data: 'budget', 'id', 'popularity' and 'release_date' columns
                have consistent and appropriate data types, no any errors would be raised.
                when use astype(), to_numeric() and to_datetime() funtions.
                
Assumption 5: The common column for merge dataframe would be unchanged. Merge two dataframes, 
              wiki_data and kaggle_data, woulbe be on 'imdb_id' column.
                
Assumption 6: The movielens_ratings dataset would be able to groupby two columns 'movieId','rating'.

Assumption 7: The PostgreSQL owner and server names keep unchanged. 
