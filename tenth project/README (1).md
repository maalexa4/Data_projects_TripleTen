
# Gold Recovery Prediction Model for Zyfra

## Project Description
This project involves developing a machine learning model to predict the amount of gold recovered from gold ore in the gold mining sector, specifically for Zyfra. Zyfra develops efficiency solutions for heavy industries, and this model aims to optimize the production process and eliminate unprofitable parameters. The data includes details on the extraction and purification stages of the ore processing.

### Problem Addressed
The model is designed to predict the recovery rate of gold from the rougher and final concentrate processes, which are critical stages in gold ore processing. Accurate predictions will help the company optimize its operations and reduce losses.

### Data Analysis and Model Development
- **Data Preparation:** The dataset provided by Zyfra includes raw material parameters, process stages, and output data. These were cleaned and processed for analysis.
- **Feature Engineering:** The features were carefully engineered based on the stages of the gold recovery process, including parameters like air amount, fluid levels, feed size, and feed rate.
- **Modeling:** Various machine learning models were trained and tested to predict the recovery rates. The final model was chosen based on its performance on the evaluation metric, sMAPE (symmetric Mean Absolute Percentage Error).

### Tools Used
- **Python**: The primary programming language.
- **Pandas**: For data manipulation and analysis.
- **Matplotlib**: For data visualization.
- **Sklearn**: For model development and evaluation.

### Key Insights
- The recovery process is highly dependent on the stability of the flotation and purification stages.
- Feature importance analysis showed that feed size and air amount are critical factors influencing gold recovery.
- The final model showed promising results with a low sMAPE, indicating its effectiveness in predicting gold recovery rates.

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
2. Train the model:
    ```bash
    python src/train_model.py
    ```
3. Evaluate the model:
    ```bash
    python src/evaluate_model.py
    ```

## Future Improvements
- **Improve Feature Engineering**: Incorporate more domain-specific knowledge to enhance feature engineering.
- **Model Refinement**: Experiment with advanced ensemble methods and hyperparameter tuning to improve accuracy.
- **Real-time Prediction**: Develop a pipeline for real-time prediction and monitoring of gold recovery rates.

## Contributors
This project was developed as part of the Zyfra Gold Recovery Prediction Challenge.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
