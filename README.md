# Movies-ETL Extract, Transder, Load

## Project Overview
Amazing Prime would like to develop an algorithm to predict which low budget movie released will become popular, so they can buy streaming rights at first. This project is to extract and prepare data for Amazing Prime video platform. Three data sources are released and used from Amazing Prime: a scrape of Wikipedia of all movies released since 1990, a collections of movie data from Kaggle, and a rating data for those movies from the Movie Land's website. This project will extract data from Wikipedia and kaggle, clean and structure data in a desired form, compare and drop unnecessary data, then join the data with ratings, and load the prepared data to SQL.

### To clean Wikipedia : 
- Load the Wikipedia data into dataframe
- Inspect and Drop duplicated movies
- Check current keys and transform different language names into one additional column "alternative name"
- Define functions to change columns' names
- Drop columns with over 90% of NaNs
- Structure data types and forms for numeric columns by using regex to extract and transform: box office, budget, running time, and release date.

### To clean kaggle:
- Inspect and drop repeated movies
- Drop adult movies
- Transform several columns to their appropriate data types: video(boolean), budget(int), id(int), popularity(int), release date(date), runtime(int)

### Join tables
- Compare Wikipedia and Kaggle's similar columns and pick more useful ones, then join two tables into movies_df.
- Load and Group ratings by movies' ID and ratings
- Merge movies_df with ratings.

### Load data to SQL
- load movies with ratings into SQL.
