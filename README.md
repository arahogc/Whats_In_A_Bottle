# Whats_In_A_Bottle
Group project to determine how which wines are good based on consumer reports and contents of the wine

### Links to csv files in s3:
* Raw Data File: [winemag-data_first150k.csv](https://whats-in-a-bottle.s3-us-west-1.amazonaws.com/winemag-data_first150k.csv)

* Rescaled Data File: [winemag-data_rescaled.csv](https://whats-in-a-bottle.s3-us-west-1.amazonaws.com/winemag-data_rescaled.csv)
    * This file contains the tokenized, filtered, and hashed values from the [description] column in addition to the original column. Column [region_2] was dropped and null values in the [designation] and [region_1] columns were replaced with "N/A". Remaining rows with null values were then removed.

* Binned Data File: [winemag-data_binned.csv](https://whats-in-a-bottle.s3-us-west-1.amazonaws.com/winemag-data_binned.csv)
    * This file contains the information for the rescaled data file, but the categorical columns have been binned to reduce the number of unique values in each column.

* **Cleaned Data File:** [winemag-data_cleaned.csv](https://whats-in-a-bottle.s3-us-west-1.amazonaws.com/winemag-data_cleaned.csv)
    * **Download this file to use for model training**
    * All columns have been converted to numeric data types and categorical columns have been encoded. Additionally, the [features] column, which originally contained a list of lists in each row, have been separated so that each number is now in it's own column. These columns are labeled with numbers staring at '1'. Wines with longer descriptions had more features, and thus fill up more columns for the separated features than shorter descriptions. 

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

### Outline
![](Resources/Images/outline.png)

Outline of the resources and technologies that will be used during this project. Subject to change. 