# What Drives the Price of a Car?

## Introduction
This project aims to understand the factors that influence car prices. The objective is to provide clear recommendations to a used car dealership regarding what consumers value in a used car.

The Jupyter notebook contains the analysis and recommendations based on the dataset provided. The analysis includes data cleaning, exploratory data analysis, feature engineering, regression modeling, and feature importance analysis and can be found [here](https://github.com/Michael-Stout/Module_11/blob/master/src/prompt_II.ipynb).

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

## Results

<img src="https://github.com/Michael-Stout/Module_11/blob/master/images/feature_importances.png" class="center" style="width:600px;height:auto;">

The provided chart displays the feature importances for a linear regression model, visualized through the coefficients assigned to each feature. Here is an interpretation of these results:

1. **Year**:
   - This feature has the highest positive coefficient, indicating that it is the most influential predictor in increasing the dependent variable (likely price or value of a vehicle).
   - A newer vehicle year significantly increases the predicted value.

2. **Manufacturer**:
   - This feature also has a high positive coefficient, suggesting that the make of the vehicle is a strong positive predictor of its value.
   - Certain manufacturers likely contribute more positively to the vehicle's value.

3. **Fuel**:
   - This feature has a positive coefficient, indicating that the type of fuel (e.g., gasoline, diesel) positively influences the predicted value.
   - Specific fuel types might be more desirable, thus increasing the vehicle's value.

4. **Odometer**:
   - This feature has a significant negative coefficient, meaning that higher mileage on the odometer reduces the vehicle's predicted value.
   - More miles driven usually correlate with wear and tear, thus decreasing the vehicle's value.

5. **Title Status**:
   - This feature has a small positive coefficient, suggesting it has a minimal but positive influence on the predicted value.
   - A clean title status might slightly increase the vehicle's value.

6. **Transmission**:
   - This feature has a moderate positive coefficient, indicating that certain transmission types (e.g., automatic, manual) positively affect the predicted value.
   - Specific transmission types may be more sought after, thus increasing the vehicle's value.

7. **Drive**:
   - This feature has a positive coefficient, suggesting that the drivetrain (e.g., FWD, RWD, AWD) positively influences the vehicle's value.
   - Certain drivetrains may be more desirable, hence increasing the vehicle's value.

8. **Type**:
   - This feature has a significant positive coefficient, indicating that the vehicle type (e.g., SUV, sedan) positively impacts the predicted value.
   - Specific vehicle types might be more popular, thus increasing the vehicle's value.

9. **Paint Color**:
   - This feature has a minimal impact as its coefficient is close to zero, indicating that the color of the vehicle is not a strong predictor of its value.

10. **Cylinders**:
    - This feature has a moderate positive coefficient, suggesting that the number of cylinders in the engine positively influences the predicted value.
    - Vehicles with more cylinders might be more powerful and desirable, thus increasing the vehicle's value.

Overall, the model indicates that the year of the vehicle is the most critical factor in predicting its value, followed by the manufacturer, odometer reading, and other features such as fuel type, cylinders, and vehicle type. Negative coefficients like the odometer reading decrease the value, while positive coefficients increase it.

## Recommendations

Based on the analysis of feature importances via coefficients from a Linear Regression model, here are clear recommendations on what consumers value in a used car:

1. **Focus on Newer Models**:
   - **Observation**: The year of the car is the most significant positive feature.
   - **Recommendation**: Prioritize acquiring and selling newer car models. Promote the newer models as they significantly increase consumer willingness to pay a higher price.

2. **Highlight Popular Brands**:
   - **Observation**: Manufacturer is a substantial positive factor.
   - **Recommendation**: Stock and emphasize vehicles from well-known and reputable manufacturers. Market the brand prominently as consumers are willing to pay more for cars from desirable brands.

3. **Promote High-Performance Vehicles**:
   - **Observation**: Number of cylinders positively affects price.
   - **Recommendation**: Highlight cars with more cylinders and market them as high-performance or luxury vehicles. Educate consumers on the benefits of having a more powerful engine to justify higher prices.

4. **Fuel Type as a Selling Point**:
   - **Observation**: Fuel type has a positive impact on price.
   - **Recommendation**: Emphasize vehicles with more desirable fuel types, such as hybrids or electric cars, which are becoming increasingly popular. Promote the benefits of these fuel types in terms of efficiency and environmental impact.

5. **Diverse Vehicle Types**:
   - **Observation**: Vehicle type (e.g., SUV, truck) significantly impacts price.
   - **Recommendation**: Maintain a diverse inventory that includes various vehicle types. Highlight the specific benefits and uses of different types, such as the versatility of SUVs or the utility of trucks.

6. **Drive Type Matters**:
   - **Observation**: Drive type (e.g., AWD, FWD) positively impacts price.
   - **Recommendation**: Stock vehicles with popular drive types like All-Wheel Drive (AWD) and promote their advantages, such as better handling and performance in various driving conditions.

7. **Minimize High Mileage Vehicles**:
   - **Observation**: Higher odometer readings (mileage) drastically reduce the car price.
   - **Recommendation**: Avoid acquiring high-mileage vehicles. If you must stock them, ensure they are priced competitively. Emphasize maintenance records and any recent overhauls or repairs to mitigate consumer concerns about high mileage.

8. **Transmission Preferences**:
   - **Observation**: Transmission type has a small negative impact on price.
   - **Recommendation**: Be aware of consumer preferences for transmission types in your market. While the impact is small, promoting the advantages of automatic transmissions, if preferred, could help in quicker sales.

9. **Title Status and Transparency**:
   - **Observation**: Title status has a small negative impact.
   - **Recommendation**: Ensure transparency about the vehicle’s title status. If the title status is less favorable, provide detailed history and reasons to build consumer trust and potentially justify the pricing.

10. **Deemphasize Paint Color**:
    - **Observation**: Paint color has a negligible impact on price.
    - **Recommendation**: While maintaining a variety of colors is good, don't overly focus on paint color as a selling point. Instead, ensure the quality and condition of the paint job, as well-maintained exteriors are generally expected.

### Summary

Consumers value newer models, reputable brands, high-performance engines, desirable fuel types, and certain vehicle types and drive configurations. High mileage and less favorable title statuses negatively impact price perceptions. Use these insights to strategically acquire inventory, highlight key features in marketing, and set pricing to align with consumer preferences.