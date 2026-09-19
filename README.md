Sports Salary Analysis Project

This project uses SQLite DB Browser to analyze and compare player salaries across major sports leagues. The goal is to calculate key metrics like maximum, minimum, and average salaries by position to see how different leagues distribute their money.

 leagues analyzed so far:
- NBA (Basketball) 2022-23

Project File Structure
- NBA Salaries by Position (2022-23).db: The SQLite database holding the raw and processed basketball data.
- NBA Salaries by Position (2022-23).sqbpro: The DB Browser workspace settings file.
- query.sql: The SQL script used to clean the data and calculate the metrics.

NBA Analysis (2022-23 Season)

Dataset Source
The data comes from Jamie Welsh's "NBA Player Salaries (2022-23 Season)" dataset on Kaggle. 
Link: https://www.kaggle.com/datasets/jamiewelsh2/nba-player-salaries-2022-23-season

Data Cleaning & Fixes
When importing the original CSV file into SQLite, the tool defaults the salary column to a text data type instead of numbers. Because of this, standard SQL math gives incorrect results (for example, reading 900,000 as higher than 48,000,000 because 9 is alphabetically bigger than 4). 

The query.sql file fixes this by using a CAST statement to force SQLite to read the salaries as actual numeric values before finding the maximum and average values for each position.

[Future sports analyses like NFL, MLB, and Premier League will be added here as the datasets are processed]
