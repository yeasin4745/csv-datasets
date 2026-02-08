# Machine Learning Datasets Collection

This repository serves as a curated collection of diverse datasets suitable for various machine learning tasks. The datasets are organized into categories based on their primary application (e.g., regression, classification, time series) to facilitate easy access and use for training and evaluating machine learning models.

## Table of Contents

- [Dataset Categories](#dataset-categories)
- [Existing Datasets](#existing-datasets)
  - [Regression Datasets](#regression-datasets)
  - [JSON Data](#json-data)
- [Newly Added Datasets](#newly-added-datasets)
  - [Classification Datasets](#classification-datasets)
  - [Time Series Datasets](#time-series-datasets)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Dataset Categories

The datasets are structured into the following directories:

*   `datasets/regression/`: Contains datasets primarily used for regression tasks.
*   `datasets/classification/`: Contains datasets suitable for classification tasks.
*   `datasets/time_series/`: Contains datasets for time series analysis and forecasting.
*   `datasets/json_data/`: Contains JSON formatted data, potentially for NLP or question-answering tasks.

## Existing Datasets

### Regression Datasets

#### `datasets/regression/student_scores.csv`

*   **Description**: This dataset contains information about student study habits and their corresponding scores. It can be used to predict student performance based on study hours and sleep patterns.
*   **Columns**:
    *   `Hours_Studied`: Number of hours a student studied.
    *   `Sleep_Hours`: Number of hours a student slept.
    *   `Score`: The score obtained by the student.
*   **Potential ML Task**: Regression (e.g., predicting `Score`).

#### `datasets/regression/height_weight.csv`

*   **Description**: A simple dataset correlating height and weight. Useful for basic linear regression examples.
*   **Columns**:
    *   `Height_cm`: Height of an individual in centimeters.
    *   `Weight_kg`: Weight of an individual in kilograms.
*   **Potential ML Task**: Regression (e.g., predicting `Weight_kg` from `Height_cm`).

#### `datasets/regression/housing_market_data.csv`

*   **Description**: Contains synthetic data related to housing market properties, including size, number of bedrooms, year built, and price. Ideal for predicting house prices.
*   **Columns**:
    *   `Size_sqft`: Size of the house in square feet.
    *   `Bedrooms`: Number of bedrooms.
    *   `Year_Built`: Year the house was built.
    *   `Price`: The selling price of the house.
*   **Potential ML Task**: Regression (e.g., predicting `Price`).

### JSON Data

#### `datasets/json_data/iq_questions.json`

*   **Description**: A collection of IQ test questions, including number series, analogies, odd-one-out, pattern recognition, logical reasoning, and arithmetic logic. Each question has options and a correct answer.
*   **Structure**: A JSON array of objects, each with:
    *   `question`: The question text.
    *   `options`: An array of possible answers.
    *   `answer`: The correct answer.
    *   `type`: The category of the question (e.g., "Number Series", "Analogy").
*   **Potential ML Task**: Natural Language Processing (NLP), Question Answering, Text Classification.

## Newly Added Datasets

### Classification Datasets

#### `datasets/classification/flower_species.csv`

*   **Description**: A synthetic dataset inspired by the Iris dataset, containing measurements of different flower species. Useful for multi-class classification problems.
*   **Columns**:
    *   `SepalLength`: Sepal length of the flower.
    *   `SepalWidth`: Sepal width of the flower.
    *   `PetalLength`: Petal length of the flower.
    *   `PetalWidth`: Petal width of the flower.
    *   `Species`: The species of the flower (target variable).
*   **Potential ML Task**: Multi-class Classification (e.g., predicting `Species`).

#### `datasets/classification/customer_churn.csv`

*   **Description**: A synthetic dataset containing customer information and whether they churned (stopped using a service). Ideal for binary classification to predict customer churn.
*   **Columns**:
    *   `CustomerID`: Unique identifier for each customer.
    *   `Age`: Age of the customer.
    *   `MonthlyCharges`: Monthly charges for the service.
    *   `TotalUsage_GB`: Total data usage in GB.
    *   `ContractType`: Type of contract (e.g., Month-to-month, One year, Two year).
    *   `Churn`: Binary indicator (0 for no churn, 1 for churn).
*   **Potential ML Task**: Binary Classification (e.g., predicting `Churn`).

#### `datasets/classification/diabetes_prediction.csv`

*   **Description**: A synthetic dataset for predicting diabetes based on various health metrics. Useful for medical classification tasks.
*   **Columns**:
    *   `Age`: Age of the patient.
    *   `BMI`: Body Mass Index.
    *   `BloodPressure`: Blood pressure reading.
    *   `Glucose`: Glucose level.
    *   `Outcome`: Binary indicator (0 for no diabetes, 1 for diabetes).
*   **Potential ML Task**: Binary Classification (e.g., predicting `Outcome`).

### Time Series Datasets

#### `datasets/time_series/stock_prices.csv`

*   **Description**: A synthetic time series dataset representing daily stock prices and trading volumes. Suitable for time series forecasting and analysis.
*   **Columns**:
    *   `Date`: The date of the observation.
    *   `Close_Price`: The closing price of the stock.
    *   `Volume`: The trading volume for the day.
*   **Potential ML Task**: Time Series Forecasting (e.g., predicting future `Close_Price`).

## Usage

To use these datasets, first clone the repository:

```bash
git clone https://github.com/yeasin4745/csv-datasets.git
cd csv-datasets
```

Then, you can access the datasets from their respective directories (e.g., `datasets/regression/student_scores.csv`). You can use libraries like Pandas in Python to load and manipulate these datasets:

```python
import pandas as pd

# Load a regression dataset
student_scores_df = pd.read_csv("datasets/regression/student_scores.csv")
print(student_scores_df.head())

# Load a classification dataset
flower_species_df = pd.read_csv("datasets/classification/flower_species.csv")
print(flower_species_df.head())

# Load a time series dataset
stock_prices_df = pd.read_csv("datasets/time_series/stock_prices.csv")
print(stock_prices_df.head())

# Load JSON data
import json
with open("datasets/json_data/iq_questions.json", "r") as f:
    iq_data = json.load(f)
print(iq_data[0])
```

## Contributing

Contributions of new, high-quality, and diverse datasets are highly welcome! Please ensure that any new datasets are clean, well-formatted, and include a brief description of their content and potential use cases. Feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.
