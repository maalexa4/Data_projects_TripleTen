
# Insurance Benefits Prediction and Data Obfuscation for Sure Tomorrow

## Project Description
This project was developed to solve several tasks for the Sure Tomorrow insurance company using Machine Learning. The tasks include identifying similar customers, predicting insurance benefits, and protecting client data through obfuscation while maintaining model performance.

### Problem Addressed
1. **Customer Similarity Search:** Identify customers similar to a given customer to assist in targeted marketing.
2. **Insurance Benefit Prediction:** Develop a classification model to predict whether a new customer is likely to receive an insurance benefit.
3. **Benefit Quantity Prediction:** Use linear regression to predict the number of insurance benefits a new customer is likely to receive.
4. **Data Obfuscation:** Implement a data transformation algorithm to protect client data without degrading the model's performance.

### Data Analysis and Model Development
- **Data Preprocessing:** The dataset was cleaned, and features were selected for analysis and model training.
- **Feature Engineering:** Scaling and transformation techniques were used to prepare the data for machine learning models.
- **Modeling:** Different models, including k-Nearest Neighbors and Linear Regression, were implemented and evaluated.
- **Data Obfuscation:** A random matrix transformation was applied to obfuscate sensitive personal data while allowing the recovery of the original data for analysis.

### Tools Used
- **Python**: The primary programming language.
- **Pandas**: For data manipulation and analysis.
- **Scikit-learn**: For machine learning model development.
- **Seaborn & Matplotlib**: For data visualization.

### Key Insights
- **kNN Classifier:** The classifier performed well after scaling the data, showing a significant improvement in F1 score.
- **Linear Regression:** The model provided reasonable predictions for the number of insurance benefits and maintained performance even with obfuscated data.
- **Data Obfuscation:** The data transformation technique successfully protected client information without compromising the model's predictive capabilities.

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
1. Run the data preprocessing script:
    ```bash
    python src/data_preprocessing.py
    ```
2. Train the kNN and Linear Regression models:
    ```bash
    python src/train_knn.py
    python src/train_linear_regression.py
    ```
3. Evaluate the model and perform data obfuscation:
    ```bash
    python src/evaluate_model.py
    python src/data_obfuscation.py
    ```

## Future Improvements
- **Enhanced Feature Selection:** Explore additional features that could improve the predictive performance of the models.
- **Advanced Obfuscation Techniques:** Implement and test other data obfuscation techniques that might provide even better security while maintaining model performance.
- **Deployment:** Create a pipeline for real-time deployment of the models for use in production environments.

## Contributors
This project was developed as part of the Sure Tomorrow Insurance Benefits Prediction Challenge.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
