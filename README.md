# What Drives the Price of a Car?

## Introduction
This project aims to understand the factors that influence car prices. The objective is to provide clear recommendations to a used car dealership regarding what consumers value in a used car.

## Methodology
The methodology for this assignment follows the CRISP-DM framework and includes standard machine learning stages such as Business Understanding, Data Understanding, Data Preparation, Modeling, and Evaluation. 

## Data Quality and Preparation
The dataset had significant missing values, duplicates, and outliers in a few categories. Data preparation and cleaning techniques had a substantial impact on the outcome. I used deduplication and imputation techniques on missing values and mean-ecoding for non-numeric variables. I used Z-Scoring for numeric outliers.
## Regression Models and Performance
I used the following models:
1. Linear Regression
2. Ridge Regression with default parameters
3. Ridge Regression with optimal alpha using GridSearchCV
4. Lasso Regression with various parameters
5. RidgeCV with target log transformation

Surprisingly, all models scored roughly the same for training and test scores.

## Feature Importance
I assessed feature importance by examining the coefficients of the linear models. The "odometer" variable showed a strong negative relationship with the price target, indicating that the more miles on a car, the less valuable it becomes. Six other variables displayed sizeable effects on the price.

## Results and Discussion
The analysis reveals that the odometer reading and the year of manufacture are the most influential factors in determining a car's price. Higher odometer values negatively impact the price, while older cars are less valuable.

## Recommendation

Based on our analysis, the two most important properties influencing a used car's price are its current mileage and the year it was manufactured. Customers are willing to pay more for vehicles with lower mileage and those manufactured in recent years.

When purchasing a used car at auction

Focus on the mileage and model year rather than the other features and prioritize buying cars manufactured in recent years with low odometer readings.