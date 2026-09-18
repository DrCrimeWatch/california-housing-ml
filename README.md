# California Housing Machine Learning Assignment

## Assignment Overview
This assignment explores the California Housing dataset and applies machine
learning regression techniques to predict median house values. Linear
Regression and Ridge Regression are compared using 5-fold cross-validation.

## Dataset
The target variable is `MedHouseVal`, which represents the median house value.

The input features are:
- MedInc
- HouseAge
- AveRooms
- AveBedrms
- Population
- AveOccup
- Latitude
- Longitude

## Data Preprocessing
StandardScaler was used to standardize the numerical features so that features
with different numerical ranges are placed on a common scale.

## Models Used
- Linear Regression
- Ridge Regression with alpha values of 0.1, 10, and 1000

## Model Evaluation
The models were evaluated using 5-fold cross-validation with R² as the
evaluation metric.

| Model | Alpha | Mean 5-Fold CV R² |
|---|---:|---:|
| Linear Regression | N/A | 0.6457 |
| Ridge Regression | 0.1 | 0.6457 |
| Ridge Regression | 10 | 0.6443 |
| Ridge Regression | 1000 | 0.3574 |

## Key Findings
Linear Regression and Ridge Regression with small to moderate alpha values
produced similar results. Ridge Regression applies a penalty to large
coefficients to reduce overfitting. However, when alpha was increased to
1000, the model became overly restricted and underfit the data, resulting
in a significantly lower R² score.

Five-fold cross-validation provides a more reliable estimate of model
performance than a single train/test split because the model is evaluated
on multiple portions of the dataset and the results are averaged.

## Tools and Libraries
- Python
- Google Colab
- pandas
- scikit-learn
- Matplotlib