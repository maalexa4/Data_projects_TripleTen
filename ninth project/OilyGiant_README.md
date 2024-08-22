
# OilyGiant Mining Company: Optimal Location for a New Well

## Introduction

This project aims to assist the OilyGiant mining company in identifying the best location for a new oil well. The process involves analyzing data from three different regions, building predictive models to estimate the volume of reserves in new wells, and selecting the region that offers the highest potential profit while minimizing risks.

## Project Steps

1. **Data Collection**: 
   - Gather oil well parameters from three regions, including oil quality and reserve volume.
   - The data includes three datasets: `geo_data_0.csv`, `geo_data_1.csv`, and `geo_data_2.csv`.

2. **Model Building**:
   - A Linear Regression model was built to predict the volume of reserves in the new wells based on the provided features.
   - The model was trained and validated for each region separately.

3. **Profit Calculation**:
   - The profitability of each region was calculated based on the predicted reserve volumes and associated revenue.
   - Bootstrapping was used to assess potential profits and risks, considering the variability in predictions.

4. **Region Selection**:
   - Regions were evaluated based on their expected profit and the risk of losses.
   - The region with the highest expected profit and the lowest risk was selected as the best location for the new well.

## Data Preparation

- The data from all three regions was loaded and checked for missing values, duplicates, and correct data types.
- No missing values or duplicates were found, and all data types were appropriate for analysis.

## Model Training and Testing

- **Data Splitting**: Each region's data was split into training and validation sets (75% training, 25% validation).
- **Model Training**: A Linear Regression model was trained for each region.
- **Predictions**: The model made predictions on the validation set for each region.

### Key Findings

- **Region 0**: Average Predicted Volume = 92.40, RMSE = 37.76
- **Region 1**: Average Predicted Volume = 68.71, RMSE = 0.89
- **Region 2**: Average Predicted Volume = 94.77, RMSE = 40.15

- **Profitability Analysis**:
  - None of the regions met the required average volume per well for profitability, but Region 0 had the highest predicted profit based on the actual top wells.

## Profit Calculation and Risk Analysis

- **Bootstrapping**:
  - 1000 bootstrap samples were used to calculate the mean profit and 95% confidence intervals for each region.
  - Risk of losses (probability of negative profit) was also calculated.

### Results

- **Region 0**:
  - Mean Profit: $6,126,658.18
  - 95% Confidence Interval: [$302,321.26, $12,278,556.34]
  - Risk of Losses: 1.8%

- **Region 1**:
  - Mean Profit: $6,599,896.52
  - 95% Confidence Interval: [$1,844,591.75, $11,883,535.97]
  - Risk of Losses: 0.2%

- **Region 2**:
  - Mean Profit: $5,946,865.42
  - 95% Confidence Interval: [-$359,938.85, $12,192,224.67]
  - Risk of Losses: 3.1%

## Conclusion

**Recommended Region for New Well Development: Region 1**

### Justification:
- **Highest Mean Profit**: Region 1 is expected to generate the highest profit.
- **Lowest Risk**: Region 1 presents the lowest risk of financial losses, making it the most stable choice.
- **Better Worst-Case Scenario**: The 95% confidence interval for Region 1 indicates a more consistent profitability compared to the other regions.

By focusing on Region 1 for oil well development, OilyGiant can maximize profits and minimize financial risks.
