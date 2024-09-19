# Water Consumption Prediction using Facebook Prophet

This project utilizes the Facebook Prophet model to predict water consumption across different states of a country. It aims to help water management authorities make informed decisions based on historical water usage data. 

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Model](#model)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview
Water consumption is a critical aspect of resource management in every region. Using historical water usage data from various states, we employ the Facebook Prophet time series forecasting model to predict future trends. Prophet is especially effective for capturing seasonality and making robust forecasts even with missing data or outliers.

This repository provides a pipeline that:
1. Preprocesses water consumption data.
2. Trains the Facebook Prophet model for each state.
3. Predicts water consumption for future periods.
4. Visualizes trends and seasonal patterns in water usage.

## Features
- **State-wise Predictions:** Generate forecasts for individual states.
- **Historical Analysis:** Analyze past water consumption patterns.
- **Seasonality Detection:** Understand recurring trends in water usage.
- **Outlier Handling:** Robust performance even in the presence of anomalies in the data.
- **Easy Customization:** Add new states or modify forecast parameters with minimal effort.

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/DigvijayDutt/FbProphet.git
    cd FbProphet
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Ensure you have Python 3.x installed.

## Usage

1. Prepare your water consumption data in CSV format. The data should contain columns for:
    - `date` (in YYYY-MM-DD format)
    - `state` (the state name or identifier)
    - `consumption` (water usage in liters, gallons, etc.)

2. Run the prediction script:
    ```bash
    python predict.py --data data/water_consumption.csv --state "any state"
    ```

3. The forecast results will be saved to the `output/` directory with visualizations of predicted water usage trends.

4. Example command for predicting all states in a dataset:
    ```bash
    python predict.py --data data/water_consumption.csv --all-states
    ```

## Data
The data should contain historical water consumption records for various states. Each row should represent a single day's consumption in a given state. Here’s an example format:

| date       | state       | consumption |
|------------|-------------|-------------|
| 2021-01-01 | California  | 1000000     |
| 2021-01-02 | California  | 1100000     |
| 2021-01-01 | Texas       | 2000000     |
| 2021-01-02 | Texas       | 1900000     |

## Model
Facebook Prophet is a time-series forecasting tool developed by Facebook. It is designed to handle:
- **Seasonal effects** such as daily, weekly, and yearly trends.
- **Outliers** or anomalies in data.
- **Missing data** gaps without much loss of accuracy.

The Prophet model is trained on water consumption data for each state. The user can configure parameters such as forecasting horizon and seasonal adjustments.

## Results
The predicted water consumption for each state is visualized with confidence intervals. These plots help identify seasonal trends, anomalies, and long-term changes in consumption.

An example forecast plot:
![image](https://github.com/user-attachments/assets/dbef1917-d093-4c9c-ad06-9f2a6127143f)


## Contributing
Contributions are welcome! Please submit a pull request with any new features, optimizations, or bug fixes. You can also open an issue for discussions.
