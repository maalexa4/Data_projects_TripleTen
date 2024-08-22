
# Game Success Analysis

## Introduction

This project aims to identify patterns that determine whether a game succeeds or not, allowing us to spot potential big winners and plan effective advertising campaigns. The data used in this analysis goes back to 2016, and we have imagined the scenario as if it’s December 2016, planning a campaign for 2017. The dataset includes the ESRB ratings, which are age ratings assigned to games by the Entertainment Software Rating Board.

## Libraries Used

- **Pandas**: For data manipulation and analysis.
- **Matplotlib** and **Seaborn**: For data visualization.
- **NumPy**: For numerical operations.
- **SciPy**: For hypothesis testing.

## Data Preprocessing

### Steps:
1. **Loading the Dataset**: The dataset was loaded and displayed to understand its structure.
2. **Column Formatting**: The column names were converted to lowercase for consistency.
3. **Data Type Conversion**: 
   - `year_of_release` was converted to integer.
   - `user_score` was converted to float, replacing 'TBD' with NaN.
   - `rating` was converted to a categorical type.
4. **Handling Missing Values**:
   - Missing values in `rating` were filled with a new category 'Not Rated'.
   - Missing values in `critic_score` and `user_score` were left as NaN, considering the potential loss of valuable information if filled.
5. **Calculating Total Sales**: A new column `total_sales` was created, summing the sales across all regions.
6. **Removing Duplicates**: Duplicate rows based on `name`, `year_of_release`, and `platform` were identified and removed.

### Intermediate Conclusion:
The dataset was prepared and cleaned, making it ready for analysis. The missing values were handled appropriately, and the data was transformed to the necessary formats.

## Data Analysis

### Number of Games Released per Year
- A bar plot was created to show the number of games released each year.
- The overall trend shows growth in the number of games released annually, with peaks around 2008-2009 followed by a slight decline.

### Platform Sales Analysis
- **Top Platforms**: The platforms with the greatest total sales were identified, with the PS2 leading, followed by X360, PS3, Wii, and DS.
- **Yearly Sales Distribution**: The yearly sales distribution for different platforms from 2010 to 2016 was visualized.
- **Platform Lifespan**: Analyzed when platforms stopped making sales, indicating the average lifespan of platforms is about 9.25 years.

### Genre Sales Analysis
- **Total Sales by Genre**: Shooter, Sports, Platform, Role-Playing, and Fighting were the most profitable genres.
- **Median Sales per Game Unit by Genre**: Calculated to understand which genres have higher sales per game unit, reaffirming the profitability of the above genres.

### Regional Analysis
- **Top Platforms, Genres, and ESRB Ratings by Region**: The top five platforms, genres, and ESRB ratings were identified for North America, Europe, and Japan, showing regional variations in preferences.

## Hypothesis Testing

### Hypothesis 1: Average User Ratings of Xbox One and PC Platforms
- **Null Hypothesis (H0)**: Average user ratings of Xbox One and PC platforms are the same.
- **Result**: Failed to reject the null hypothesis, indicating no significant difference in average user ratings between Xbox One and PC platforms.

### Hypothesis 2: Average User Ratings for Action and Sports Genres
- **Null Hypothesis (H0)**: Average user ratings for Action and Sports genres are the same.
- **Result**: Failed to reject the null hypothesis, indicating no significant difference in average user ratings between Action and Sports genres.

## Conclusion
- **Platform Success**: Xbox One, PlayStation 4 (PS4), and 3DS are promising platforms.
- **Genre Success**: Shooter, Sports, and Platform genres are most profitable.
- **ESRB Ratings**: M (Mature), Not Rated, and E (Everyone) ratings are associated with better sales across regions.
- **Regional Preferences**: Differences in user preferences were observed across regions, indicating varying market dynamics and cultural influences.

This analysis provides valuable insights into the video game industry, aiding stakeholders in making informed decisions about platform selection, genre targeting, and regional marketing strategies.
