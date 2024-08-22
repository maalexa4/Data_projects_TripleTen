
# Movie Review Sentiment Analysis for Film Junky Union

## Project Description
The Film Junky Union is developing a system to filter and categorize movie reviews automatically. This project aims to train a machine learning model to detect negative reviews using a dataset of IMDb movie reviews with polarity labeling. The goal is to achieve an F1 score of at least 0.85.

### Problem Addressed
Automatically classifying movie reviews into positive and negative categories can help streamline content moderation and improve user experience. This project uses various models and text processing techniques to achieve accurate sentiment classification.

### Data Preparation
- **Text Normalization:** The review text was normalized by converting it to lowercase, removing digits, and stripping punctuation to improve the quality of the input data.
- **Dataset Splitting:** The dataset was split into training and test sets, ensuring that both sets were well-representative of the overall data distribution.

### Exploratory Data Analysis (EDA)
- **Review Trends:** Analysis revealed a consistent increase in the number of movie reviews over the years, with balanced distributions of positive and negative reviews.
- **Distribution Insights:** Movies with fewer reviews tended to receive more negative feedback, while movies with more reviews were generally better received.

### Model Training and Evaluation
Several models were trained and evaluated using the F1 score, accuracy, average precision score (APS), and ROC AUC metrics:

1. **Dummy Classifier:**
   - **Accuracy:** 0.50
   - **F1 Score:** 0.00
   - **APS:** 0.50
   - **ROC AUC:** 0.50

2. **Logistic Regression with TF-IDF (Model 1):**
   - **Accuracy:** 0.88
   - **F1 Score:** 0.88
   - **APS:** 0.95
   - **ROC AUC:** 0.95

3. **Logistic Regression with TF-IDF and spaCy (Model 3):**
   - **Accuracy:** 0.88
   - **F1 Score:** 0.88
   - **APS:** 0.95
   - **ROC AUC:** 0.95

4. **LightGBM with TF-IDF and spaCy (Model 4):**
   - **Accuracy:** 0.86
   - **F1 Score:** 0.86
   - **APS:** 0.93
   - **ROC AUC:** 0.94

### Key Insights
- **Logistic Regression Performance:** The logistic regression model, combined with TF-IDF vectorization, consistently achieved high performance, meeting the project's goal with an F1 score of 0.88.
- **Text Preprocessing:** The normalization process significantly enhanced the quality of the input text, leading to better model performance.
- **Model Selection:** Logistic regression outperformed other models, although LightGBM also showed strong results, particularly in terms of APS and ROC AUC.

### Conclusion
The logistic regression model, using TF-IDF vectorization and simple text preprocessing, effectively classified movie reviews as positive or negative. The model achieved an F1 score of 0.88 on the test set, surpassing the project's requirement of 0.85. This approach proves to be reliable for sentiment analysis in movie reviews, with potential for further improvement through ensemble methods or additional feature engineering.

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
- **Ensemble Methods:** Combining models, such as logistic regression and LightGBM, could enhance classification accuracy.
- **Feature Engineering:** Incorporating additional features like sentiment scores or part-of-speech tags might improve model performance.
- **Real-time Sentiment Analysis:** Implement a real-time analysis pipeline to classify incoming reviews instantly.

## Contributors
This project was developed as part of a movie review sentiment analysis challenge for the Film Junky Union.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
