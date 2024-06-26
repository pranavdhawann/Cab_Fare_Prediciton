## Overview

This project aims to predict Uber fare prices based on various factors such as distance, time of day, and location. It utilizes machine learning models to provide accurate fare estimates to users.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Models](#models)
- [Evaluation](#evaluation)
- [Contributing](#contributing)
- [License](#license)

## Dataset

The project uses a dataset sourced from Uber's public data repository, consisting of over 100,000 ride records. Each record includes information as listed below:
Data columns (total 19 columns):
 #   Column                 Non-Null Count   Dtype  
---  ------                 --------------   -----  
 0   VendorID               100000 non-null  int64  
 1   tpep_pickup_datetime   100000 non-null  object 
 2   tpep_dropoff_datetime  100000 non-null  object 
 3   passenger_count        100000 non-null  int64  
 4   trip_distance          100000 non-null  float64
 5   pickup_longitude       100000 non-null  float64
 6   pickup_latitude        100000 non-null  float64
 7   RatecodeID             100000 non-null  int64  
 8   store_and_fwd_flag     100000 non-null  object 
 9   dropoff_longitude      100000 non-null  float64
 10  dropoff_latitude       100000 non-null  float64
 11  payment_type           100000 non-null  int64  
 12  fare_amount            100000 non-null  float64
 13  extra                  100000 non-null  float64
 14  mta_tax                100000 non-null  float64
 15  tip_amount             100000 non-null  float64
 16  tolls_amount           100000 non-null  float64
 17  improvement_surcharge  100000 non-null  float64
 18  total_amount           100000 non-null  float64

## Installation 

To run the project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/pranavdhawann/UberFarePredictor.git
   cd UberFarePredictor
   ```
2. Install dependencies:
   ```
   python -m venv uber
   uber/Scripts/activate
   pip install -r requirements.txt

## Models

### Linear Regression
Linear Regression is employed as a fundamental model for predicting Uber fares by establishing a linear relationship between predictor variables (such as distance, time, and location) and the fare amount. It assumes a linear combination of these variables to estimate fare prices, making it straightforward to interpret and compute. This model serves as a baseline for understanding the direct impact of each predictor on fare predictions.

### Random Forest
The Random Forest model is utilized as an ensemble learning method to enhance prediction accuracy by capturing complex, non-linear relationships in the data. It operates by constructing multiple decision trees during training and averaging their predictions to produce a final fare estimate. This approach enables the model to handle interactions between variables effectively, making it robust against overfitting and noise present in real-world Uber ride data. Random Forests are particularly suitable for capturing the nuanced factors influencing fare prices, such as traffic patterns and geographical variations.

### Gradient Boosting
Gradient Boosting is employed to further improve prediction performance by sequentially refining the model's predictions through iterative training. It combines the strengths of weak learners (typically decision trees) by minimizing prediction errors, thereby reducing bias and variance. Gradient Boosting is adept at learning complex relationships in the data and can adapt to different types of features and their interactions. By iteratively correcting errors made by previous models, Gradient Boosting produces highly accurate fare predictions, making it well-suited for optimizing fare estimation in dynamic Uber ride scenarios.

## Evaluation

Based on model evaluations, Gradient Boosting yielded the lowest Mean Absolute Error (MAE), indicating superior predictive accuracy compared to Linear Regression and Random Forest. While all models effectively estimated Uber fares, Gradient Boosting's ability to minimize prediction errors through iterative refinement makes it the recommended choice for robust fare predictions. This evaluation underscores its efficacy in handling the complexities of ride data, ensuring more reliable fare estimates for practical applications.
| Model                              | MAE    |
|------------------------------------|--------|
| Linear Regression (With Outliers)   | 2.0265 |
| Linear Regression (Without Outliers)| 1.5215 |
| Random Forest (With Outliers)       | 1.5126 |
| Random Forest (Without Outliers)    | 1.3878 |
| Gradient Boosting (With Outliers)   | 1.4489 |
| Gradient Boosting (Without Outliers)| 1.3031 |

![image](https://github.com/pranavdhawann/UberFarePredictor/assets/74893835/bb2bb0d0-ef64-4fbb-aff0-1e3fa6a59057)

## Contributing

Contributions to the project are welcome! 

## License

This project is licensed under the MIT License - see the LICENSE file for details.

