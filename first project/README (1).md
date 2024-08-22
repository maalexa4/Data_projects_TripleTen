
# Golden Age of Television Analysis

## Project Overview

This project focuses on analyzing data from the entertainment industry, specifically investigating how the number of votes a TV show receives impacts its ratings during the "Golden Age" of television, which began in 1999 with the release of *The Sopranos* and continues to this day.

### Objective

The primary objective of this project is to determine whether highly-rated TV shows from the "Golden Age" of television also receive the most votes on IMDb. This analysis aims to explore the relationship between ratings and the number of votes to draw insights about audience engagement with these shows.

### Dataset

The dataset used in this project contains records of movies and TV shows, including details such as title, release year, genres, IMDb scores, and IMDb votes. The dataset is stored in the file `/datasets/movies_and_shows.csv`.

## Project Stages

### 1. Data Overview

In the initial stage, the dataset was explored to understand its structure and identify any potential issues. Key findings include:

- The dataset contains 85,579 entries with 9 columns.
- Some columns had missing values, and the column names required formatting corrections.
- Initial exploration revealed that three columns had missing values: 'title', 'imdb_score', and 'imdb_votes'.

### 2. Data Preprocessing

During data preprocessing, the following steps were taken:

- Column names were standardized by removing whitespace, correcting capitalization, and fixing typos.
- Rows with missing values in 'imdb_score' and 'imdb_votes' were dropped, as these values are crucial for the analysis.
- Duplicates and implicit duplicates were identified and removed to ensure the accuracy of the analysis.

### 3. Data Analysis

In the final stage, the prepared data was analyzed to investigate the relationship between IMDb scores and the number of votes:

- TV shows released after 1999 were isolated, and the data was filtered to focus on shows with IMDb scores between 4 and 9.
- The analysis revealed that shows with higher IMDb scores tend to receive more votes, with the top three score categories (7-9) having the most significant number of votes.

## Findings

The analysis confirmed the initial hypothesis: highly-rated TV shows released during the "Golden Age" of television also receive the most votes. This suggests that shows with higher ratings attract more viewers, leading to more votes.

## Tools and Technologies

- **Pandas**: For data manipulation and analysis.
- **Jupyter Notebook**: For running and documenting the analysis.
- **Python**: The programming language used for all data processing tasks.

## Future Improvements

1. **Expand Analysis**: Extend the analysis to include more years and investigate whether the trend holds in other time periods.
2. **Feature Engineering**: Explore additional features such as genre and cast popularity to see how they influence ratings and votes.
3. **Visualization**: Create visualizations to better communicate the results of the analysis.

## Usage Instructions

### Requirements

- **Python 3.8+**
- **Pandas**
- **Jupyter Notebook**

### Running the Project

1. Clone the repository to your local machine.
2. Ensure you have the required packages installed.
3. Open the Jupyter Notebook and run the cells sequentially to reproduce the analysis.

## Conclusion

This project successfully identified a positive correlation between high ratings and the number of votes for TV shows released during the "Golden Age" of television. The findings contribute to a better understanding of audience engagement in the entertainment industry.
