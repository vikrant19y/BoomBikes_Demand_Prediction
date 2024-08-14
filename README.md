# BoomBike Demand Prediction using Linear Regression
> Prediction of Demand for Shared Bikes using Multiple Linear Regression

## Table of Contents

* [General Information](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information

### [1. Introduction](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#intro)

#### [1.1. Problem Statement](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#problem)

Bike-sharing systems provide bikes for shared use, allowing individuals to rent bikes for short periods, either for a fee or free of charge. BoomBikes, a US-based bike-sharing provider, has experienced a sharp decline in revenue due to the COVID-19 pandemic. To counter this, the company aims to create a strategic business plan to boost revenue once the lockdown is lifted and the economy recovers.

The company seeks to understand the factors that influence the demand for shared bikes in the American market. Specifically, BoomBikes wants to determine:
- Which variables are significant in predicting the demand for shared bikes.
- How well these variables explain the fluctuations in bike demand.

#### [1.2. Business Goal](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#goal)

The objective is to develop a predictive model for bike demand using the available independent variables. This model will provide insights into the demand dynamics, enabling the management to fine-tune their business strategy to better meet customer needs and gain a competitive advantage in the market.

#### [1.3. Dataset Overview](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#dataoverview)

The dataset includes daily records of bike demand across the American market, capturing various factors such as weather conditions, seasonality, and user behavior. Key columns in the dataset include:

- **instant**: Record index
- **dteday**: Date
- **season**: Season (1: Spring, 2: Summer, 3: Fall, 4: Winter)
- **yr**: Year (0: 2018, 1: 2019)
- **mnth**: Month (1 to 12)
- **holiday**: Whether the day is a holiday (extracted from [Holiday Schedule](http://dchr.dc.gov/page/holiday-schedule))
- **weekday**: Day of the week
- **workingday**: Whether the day is neither a weekend nor a holiday (1 if true, otherwise 0)
- **weathersit**: Weather situation
  - 1: Clear, Few clouds, Partly cloudy
  - 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds
  - 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds
  - 4: Heavy Rain + Ice Pellets + Thunderstorm + Mist, Snow + Fog
- **temp**: Temperature in Celsius
- **atemp**: Feels-like temperature in Celsius
- **hum**: Humidity
- **windspeed**: Wind speed
- **casual**: Number of casual users who rented bikes
- **registered**: Number of registered users who rented bikes
- **cnt**: Total number of bike rentals (target variable)

### [2. Data Understanding and Processing](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#data)
    - 2.1. Loading the Data
    - 2.2. Initial Exploration and Dataset Characteristics
    - 2.3. Data Preprocessing

### [3. Exploratory Data Analysis](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#eda)

### [4. Feature Engineering](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#feature)

### [5. Model Building and Feature Selection](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#model)

#### [5.1. Feature Selection Using Recursive Feature Elimination (RFE)](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#rfe)
#### [5.2. Model Development and Comparison](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#models)
#### [5.3. Selecting the Best Model](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#best_model)
#### [5.4. Final Model](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#final_model)
#### [5.5. Model Evaluation](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#model_evaluation)
   - [5.5.1. Residual Analysis](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#residual_analysis)
   - [5.5.2. Predicting for Test Data](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#predicting_test_data)

## [Conclusions](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb#conclusions)

1. **Model Performance**:
   - The model shows strong performance, with an R-squared score of 0.845 on the training data and 0.806 on the testing data. This indicates that the model explains approximately 84.5% of the variance in bike demand on the training set and 80.6% on the testing set, suggesting good generalization to unseen data.

2. **Key Predictors**:
   - **Temperature (`temp`)**: The most significant positive predictor, where higher temperatures substantially increase bike demand.
   - **Year (`yr_2019`)**: A significant rise in bike demand in 2019 compared to 2018, indicating the service's growing popularity.
   - **Seasonality (`summer`, `winter`, `Jul`, `Sep`)**: Seasonal trends show increased demand in summer and winter, with a dip in July but a rise in September.
   - **Weather Conditions (`Clear`, `Light_Snow_Rain`)**: Clear weather has a positive impact on demand, while adverse conditions like light snow or rain reduce it.
   - **Day Factors**: Demand is higher on working days and Saturdays, while it decreases on holidays.

## Technologies Used

- Python - Version 3.12
- Pandas - Version 2.2.2
- NumPy - Version 1.26.4
- Matplotlib - Version 3.8.4
- Seaborn - Version 0.13.2
- Scikit-learn - Version 1.2.2
- StatsModel - Version 0.14.0

## Acknowledgements


## Contact

Created by [Vikrant Yadav](https://github.com/vikrant19y) - feel free to contact me!