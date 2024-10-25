
# Diabetes Prediction Dataset - Decision Tree Classification Model

This repository contains a Decision Tree Classification model developed for predicting diabetes based on a range of patient attributes. The project uses the **Diabetes Prediction Dataset** and focuses on building an interpretable model to classify whether an individual is likely to have diabetes.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
The goal of this project is to develop a **Decision Tree Classifier** that can predict the presence of diabetes based on features such as age, gender, BMI, blood glucose level, and other health indicators. The model is evaluated using metrics like **ROC-AUC**, **precision**, **recall**, and **accuracy** to ensure reliable performance on unseen data.

## Dataset
The dataset used in this project is the **Diabetes Prediction Dataset**, available in the `dataset/` folder:

- **Path**: `dataset/diabetes_prediction_dataset.csv`
- **Source**: [Kaggle - Diabetes Prediction Dataset](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset)
- **Features**:
  - `gender`: Gender of the individual (Male/Female/Other)
  - `age`: Age in years
  - `hypertension`: 1 if the individual has hypertension, 0 otherwise
  - `heart_disease`: 1 if the individual has any heart disease, 0 otherwise
  - `smoking_history`: Smoking habits of the individual
  - `bmi`: Body Mass Index (BMI)
  - `HbA1c_level`: Hemoglobin A1c level
  - `blood_glucose_level`: Blood glucose level
  - `diabetes`: Target variable, 1 if the individual has diabetes, 0 otherwise

## Installation
To run this project locally, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/Vishnugnath/Diabetes-Prediction-Dataset-Decision-Tree-Classification-model.git
    cd Diabetes-Prediction-Dataset-Decision-Tree-Classification-model
    ```

2. **Install required packages**:
    It is recommended to use a virtual environment:
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows: env\Scripts\activate
    pip install -r requirements.txt
    ```

## Usage
The main analysis and model training are performed in the Jupyter notebook:

- **Notebook**: `Diabetes Prediction Dataset - Decision Tree Classification model.ipynb`

To run the notebook, start Jupyter Notebook and open the file:

```bash
jupyter notebook "Diabetes Prediction Dataset - Decision Tree Classification model.ipynb"
```

## Model Training and Evaluation
The project follows these key steps:

1. **Data Understanding and Cleaning**:
   - Analyzing the structure of the dataset, checking for missing values, and ensuring data quality.
   - Encoding categorical variables and transforming skewed data.
   - Outlier detection using boxplots and treatment using IQR-based methods.

2. **Feature Engineering**:
   - Transforming features like `bmi` and `HbA1c_level` for better model performance.

3. **Model Training**:
   - Splitting the data into training and testing sets.
   - Training a **Decision Tree Classifier** with hyperparameter tuning using `GridSearchCV`.

4. **Model Evaluation**:
   - Evaluating model performance using **ROC-AUC**, **confusion matrix**, and **classification report**.
   - Visualizing the Decision Tree for interpretability.

## Results
The final Decision Tree model achieves good predictive performance with an AUC score of around **(insert AUC score)**. The model shows robust results with a balance between precision and recall, making it suitable for real-world applications.

### Example Confusion Matrix:
|   | Predicted Negative | Predicted Positive |
|---|--------------------|--------------------|
| Actual Negative | **TN** | **FP** |
| Actual Positive | **FN** | **TP** |

### Model Accuracy:
- **Training AUC**: (insert value)
- **Testing AUC**: (insert value)

## Contributing
Contributions are welcome! If you have suggestions or improvements, feel free to submit a pull request or open an issue.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
