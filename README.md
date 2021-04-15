# Whats_In_A_Bottle
Group project to determine how which wines are good based on consumer reports and contents of the wine

### Notes

4-10-21
* Created a Jupyter Notebook file that loads individual wine type csv files into DataFrames and adds an additional column for wine variety (red, white, sparkling, rose). The dataframes were concatenated to create one DataFrame with all wine information. The concatenated Dataframe was exported to a csv file [("compiled_wine.csv")](https://github.com/arahogc/Whats_In_A_Bottle/blob/Jess/Resources/compiled_wine.csv).

4-12-21
* Created a Colab notebook file that loads and cleanes the winemag-data_first150k.csv:
    * Removes columns with >50% null values
    * Replaces null values in columns we want to keep with 'N/A'
    * Drops remaining rows with null values
    * Tokenizes the description column and removes StopWords (could look into lemmatizing to get root words)
    * Encodes and scales the filtered tokens

* The cleaned (in-progess) dataframe was saved to a csv file and uploaded to S3. 

4-14-21
* Continued preprocessing the data. Binned categorical columns and encoded the dataframe. 
* ![Link to AWS S3 bucket](https://s3.console.aws.amazon.com/s3/buckets/whats-in-a-bottle?region=us-west-1&tab=objects)

### Outline
![](Resources/Images/outline.png)

Outline of the resources and technologies that will be used during this project. Subject to change. 