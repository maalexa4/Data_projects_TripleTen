
# Car Price Prediction Model

## Project Description
This project involves developing a machine learning model to predict the price of used cars. The dataset includes various features such as vehicle type, registration year, gearbox type, power, model, mileage, fuel type, and repair status. The project evaluates multiple models and compares their performance based on predictive quality and speed.

### Problem Addressed
The goal is to build an accurate and efficient model to predict the price of used cars. The models evaluated include Linear Regression and LightGBM, with the latter being tuned for optimal performance.

### Data Preparation
- **Handling Missing Values:** Missing values in categorical columns were filled with 'unknown.'
- **Feature Engineering:** Categorical features were limited to the top values and encoded using OneHotEncoder.
- **Data Sampling:** A 5% sample of the dataset was used for model training and evaluation to reduce computational load.
- **Feature Selection:** A subset of relevant features was selected to ensure a manageable number of columns (below 200).

### Model Training and Evaluation
1. **Linear Regression:**
    - **RMSE:** 3589.08
    - **Training Time:** 0.0203 seconds
    - **Prediction Time:** 0.0065 seconds
2. **LightGBM:**
    - **RMSE:** 2190.22
    - **Training Time:** 0.5684 seconds
    - **Prediction Time:** 0.0795 seconds

### Hyperparameter Tuning
- **LightGBM Tuning:** Performed using GridSearchCV with parameters like `num_leaves`, `learning_rate`, and `n_estimators`.
- **Best Parameters:** {'learning_rate': 0.1, 'n_estimators': 100, 'num_leaves': 31}
- **Tuned LightGBM RMSE:** 2151.05

### Key Insights
- **Quality vs. Speed:** LightGBM provided better predictive quality (lower RMSE) but at the cost of longer training and prediction times compared to Linear Regression.
- **Model Choice:** LightGBM is recommended for applications where prediction quality is critical. Linear Regression is preferable if speed is more important and a slight reduction in quality is acceptable.

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
- **Additional Models:** Evaluate other advanced models such as XGBoost or CatBoost for further improvement in predictive quality.
- **Feature Engineering:** Explore more feature engineering techniques to capture complex patterns in the data.
- **Real-time Prediction:** Implement real-time prediction capabilities for use in production environments.

## Contributors
This project was developed as part of a car price prediction challenge.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
