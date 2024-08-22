
# Taxi Demand Prediction Model

## Project Description
This project aims to predict the number of taxi orders in a given hour based on historical data. The data includes timestamps and the number of orders, and the goal is to develop a model that can accurately forecast demand, helping taxi companies optimize their fleet management.

### Problem Addressed
Predicting taxi demand is crucial for efficient resource allocation. This project involves training and comparing different time series models, including Linear Regression, Decision Tree, Random Forest, Gradient Boosting, and SARIMA, to determine which model provides the best predictive performance.

### Data Preparation
- **Data Resampling:** The raw data was resampled by hour to aggregate the number of taxi orders.
- **Feature Engineering:** Features such as hour, day of the week, day of the month, and month were created, along with lag and rolling mean features to capture temporal dependencies.
- **Handling Missing Values:** Missing values generated during feature creation were dropped to ensure clean data for model training.

### Model Training and Evaluation
Several models were trained and evaluated using the RMSE (Root Mean Squared Error) metric:

1. **Linear Regression:**
    - **RMSE:** 53.11

2. **Decision Tree:**
    - **RMSE:** 53.31

3. **Random Forest:**
    - **RMSE:** 46.68

4. **Gradient Boosting:**
    - **RMSE:** 47.61 (tuned model: 52.28)

5. **SARIMA:**
    - **RMSE:** 39.45 (using the last 1000 data points), 43.61 (full model)

### Key Insights
- **SARIMA Model:** The SARIMA model performed the best on the test set, achieving an RMSE of 39.45 using a small subset of the data and 43.61 with simple parameters.
- **Random Forest and Gradient Boosting:** Both models also performed well, with RMSEs below 48, making them suitable for this forecasting task.
- **Feature Importance:** Temporal features such as hour and day of the week played a significant role in predicting taxi demand.

### Conclusion
The SARIMA model using a small subset of data or simple parameters achieved the best RMSE, making it the most suitable for predicting taxi demand in this project. Other models like Random Forest and Gradient Boosting also provided competitive performance.

## Project Structure
- **data/**: Contains the raw data files used for analysis.
- **notebooks/**: Jupyter notebooks with data exploration, analysis, and model development.
- **src/**: Python scripts for data processing and model training.
- **README.md**: This file.
- **requirements.txt**: List of dependencies needed to run the project.

## Installation and Setup
To run this project, ensure you have Python 3.7+ installed. You can set up the environment using the following steps:

```bash
git clone <repository-link>
cd <project-folder>
pip install -r requirements.txt
```

## Usage
1. Run the data preparation script:
    ```bash
    python src/data_preparation.py
    ```
2. Train the models:
    ```bash
    python src/train_models.py
    ```
3. Evaluate the models:
    ```bash
    python src/evaluate_models.py
    ```

## Future Improvements
- **Advanced Model Tuning:** Further hyperparameter tuning could improve the performance of the Gradient Boosting and Random Forest models.
- **Real-time Prediction:** Implement a real-time forecasting pipeline to provide taxi demand predictions in real-time.
- **Incorporate External Data:** Integrate additional external features such as weather data, holidays, and events to improve model accuracy.

## Contributors
This project was developed as part of a taxi demand prediction challenge.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
