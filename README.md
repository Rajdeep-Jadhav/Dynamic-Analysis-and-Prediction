# AutoML Pipeline for Dynamic Data Analysis and Prediction

## Project Overview

This project is an automated machine learning pipeline designed to dynamically process any CSV dataset. It performs data cleaning, exploratory data analysis (EDA), and automatically selects and trains appropriate models for either classification or regression tasks based on the target variable. The pipeline generates visualizations, evaluates model performance, and provides predictions based on the input dataset.

## Features

- **Automated Data Loading and Preprocessing**: Automatically handles missing values, encodes categorical variables, and scales numerical features.
- **Exploratory Data Analysis (EDA)**: Generates pair plots and correlation heatmaps to provide insights into feature relationships.
- **Dynamic Model Selection**: Detects the problem type (classification or regression) based on the target variable and selects the appropriate model.
- **Model Training and Evaluation**: Trains the selected model and evaluates its performance using metrics such as accuracy, classification report, mean squared error, and R-squared.
- **Predictions on New Data**: Provides functionality to make predictions using the trained model on new datasets.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/automl-pipeline.git
    ```
2. Change into the project directory:
    ```bash
    cd automl-pipeline
    ```
3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Prepare your CSV file**: Ensure that your CSV file is formatted correctly with all the necessary features and a target column for prediction.

2. **Run the Pipeline**:
    ```python
    # Import the run_pipeline function
    from automl_pipeline import run_pipeline
    
    # Specify the file path and target column
    file_path = 'your_dataset.csv'
    target_column = 'target'
    
    # Run the pipeline
    run_pipeline(file_path, target_column)
    ```

3. **View Results**: The pipeline will output data visualizations, model performance metrics, and sample predictions.

## Functions

- **`load_data(file_path)`**: Loads the CSV file and provides a preview of the dataset.
- **`preprocess_data(df)`**: Preprocesses the dataset by handling missing values, encoding categorical features, and scaling numerical features.
- **`perform_eda(df)`**: Performs exploratory data analysis, generating pair plots and correlation heatmaps.
- **`train_model(df, target_column)`**: Automatically selects and trains a model based on the target column type (classification or regression).
- **`make_predictions(model, df, problem_type)`**: Makes predictions using the trained model on new data.
- **`run_pipeline(file_path, target_column)`**: Runs the entire pipeline from data loading to prediction.

## Example

```python
from automl_pipeline import run_pipeline

# Run the pipeline with a sample dataset
file_path = 'data/heart_disease.csv'
target_column = 'target'
run_pipeline(file_path, target_column)

