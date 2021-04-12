# Whats_In_A_Bottle
Group project to determine how which wines are good based on consumer reports and contents of the wine

## Goals:
*Basic* - Build a machine learning model that can predict wine quality based on the wine’s description, year, variety, region, and consumer reports.
 
*Intermediate goal*- give recommendations of wines based on region (e.g. “based on the description/details of this wine, this region would be preferred”)
 
*Advanced goal*- locate similar wines that nearby to user that they can buy  (e.g. “you can buy this wine at the 7/11 around the corner”)
 
### Steps to Achieve Goals:
*Basic Goal:*
- Retrieve and clean data
- Train models
- Visualize data of wine contents and consumer reports of wine
 
*Intermediate goal*
- Write for loops (or other functions that are better) that will give list of similar wines
    - Example: For wine in wine_list:
        If region is x% of wine,
        If designation is y% of wine, etc etc,
        Then add wine to recommended_list
        Print(recommended_list)
    
- Train a model on the wine magazine top 150K wines list and provide recommendations for wines from the wine variety csv files.
 
*Advanced goal*
- Use javascript/html using sales data from wine vendors to map out vendors selling recommended wines in given region (would require input from user)

### Data
- Wine variety csv files (“Red.csv”, ”White.csv”, ”Rose.csv”, ”Sparkling.csv”)
- Wine Magazine top 150K Wines ([Kaggle](https://www.kaggle.com/zynicide/wine-reviews?select=winemag-data_first150k.csv))
