
# Age Estimation Model from Images

## Project Description
This project involves building a deep learning model to estimate the age of individuals based on their images. The dataset consists of labeled images with corresponding ages, and the goal is to train a model that can accurately predict the age of a person from a given image.

### Problem Addressed
Accurately estimating age from images is useful in various applications, including age verification, demographic analysis, and personalized marketing. This project aims to develop a model that achieves low Mean Absolute Error (MAE) on a validation set, ensuring reliable age predictions.

### Data Preparation
- **Dataset:** The dataset includes 7,591 images, each labeled with the real age of the individual.
- **Image Preprocessing:** Images were rescaled and resized to 224x224 pixels. An ImageDataGenerator was used to feed the data into the model during training.
- **Age Distribution:** The dataset exhibits a wide range of ages, with a concentration in the 20-30 age range. Sample images displayed varied orientations, backgrounds, and image qualities, which are critical factors in model performance.

### Model Architecture
- **Base Model:** ResNet50 pre-trained on ImageNet, excluding the top layer.
- **Additional Layers:** GlobalAveragePooling2D, Dense layer with ReLU activation, Dropout layer, and a final Dense layer with a linear activation function for age prediction.
- **Loss Function:** Mean Absolute Error (MAE) was used as the loss function, optimized with the Adam optimizer.

### Model Training and Evaluation
The model was trained for 20 epochs with the following results:
- **Final Training MAE:** 3.18
- **Final Validation MAE:** 7.65

### Key Insights
- **Performance:** The model showed a reasonable performance with a validation MAE of 7.65 years. This indicates that the model's predictions are, on average, off by 7.65 years on the validation set.
- **Training Dynamics:** The training loss and MAE consistently decreased over the epochs, indicating effective learning. However, fluctuations in validation MAE in later epochs suggest potential overfitting.
- **Room for Improvement:** The divergence between training and validation MAE suggests overfitting. This could be addressed by implementing techniques such as early stopping, more dropout, and additional data augmentation.

### Conclusion
The model shows promising results with a validation MAE below the target threshold. However, further tuning and experimentation are needed to improve its accuracy and generalization capabilities. The findings suggest that with more refinements, the model could be effectively used in real-world applications for age estimation.

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
- **Early Stopping:** Implement early stopping to prevent overfitting during training.
- **Data Augmentation:** Increase data augmentation techniques to make the model more robust to variations in the dataset.
- **Hyperparameter Tuning:** Experiment with different learning rates, batch sizes, and model architectures to further reduce MAE.

## Contributors
This project was developed as part of an age estimation challenge.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
