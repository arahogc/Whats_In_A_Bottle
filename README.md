# Whats_In_A_Bottle

### Question: Can a machine learning model be able to predict the quality, price, region, and type of of wine based on the descriptive words and other characteristics? 

## Approach: 

### Model Development Outline
Outline of the resources and technologies that will be used during this project. Subject to change.
![](Resources/Images/outline.png)

### Data
#### Data Preprocessing 

Many, if not all, of the columns had many null values. Columns that had more than 50% than null values were dropped while the rest of the columns' null values were replaced as "N/A". This cleaned data was then futhered processed using the Natural Language Processing (NLP) by first tokenizing the description column and removing the stop words. The tokens were then counted and added to a new column. This counted token column was then encoded and binned into categorical columns with more than X unique values. This final dataframe was then checked for missing or null values and exported as a csv file to be stored in databases. Below are checkpoint files for each stop of cleaning and processing the data. 

##### S3 Files
During the preprocessing and cleaning, data was saved as csv files in s3 at multiple steps for checkpointing. If one step of the preprocessing needs to be adjusted, a checkpoint file can be imported so that the entire process does not need to be run each time. 

* Raw Data File: [winemag-data_first150k.csv](https://whats-in-a-bottle.s3-us-west-1.amazonaws.com/winemag-data_first150k.csv)
    ![](Resources/Images/raw_df.png)

* Rescaled Data File: [winemag-data_rescaled.csv](https://whats-in-a-bottle.s3-us-west-1.amazonaws.com/winemag-data_rescaled.csv)
    * This file contains the [features] values generated by tokenizing, filtering, and hashing the [description] column. Column [region_2] was dropped and null values in the [designation] and [region_1] columns were replaced with "N/A". Remaining rows with null values were then removed.
    ![](Resources/Images/rescaled_df.png)

* Description NLP File: [winemag-data_descriptionNLP.csv](https://whats-in-a-bottle.s3-us-west-1.amazonaws.com/winemag-data_descriptionNLP.csv)
    * This file contains only information relating to the description natural language processing (NLP) pipeline.
    ![](Resources/Images/descriptionNLP.png)

* Binned Data File: [winemag-data_binned.csv](https://whats-in-a-bottle.s3-us-west-1.amazonaws.com/winemag-data_binned.csv)
    * This file contains the information for the rescaled data file, but the categorical columns have been binned to reduce the number of unique values in each column.
    ![](Resources/Images/binned_df.png)

* **Cleaned Data File:** [winemag-data_cleaned.csv](https://whats-in-a-bottle.s3-us-west-1.amazonaws.com/winemag-data_cleaned_primaryKey.csv)
    * All columns have been converted to numeric data types and categorical columns have been encoded with the label encoder. The first column [_c0] is the primary key that connects the cleaned data back to the original data. Additionally, the [features] column, which originally contained a list of lists in each row, have been separated so that each number is now in it's own column. The top ten words for each wine were kept for model training:
    ![](Resources/Images/cleaned_df.png)
    ![](Resources/Images/cleaned_dtypes.png)
    
### Machine Learning Models
#### Machine Learning Process 

### Results
#### Price 
#### Quality 
#### Country 
#### Wine Type 
