# BoomBike Demand Prediction using Linear Regression
> Prediction of Demand for Shared Bikes using Multiple Linear Regression

## Table of Contents

* [General Information](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information

1. **Problem Statement**

    - BoomBikes, a US-based bike-sharing provider, has experienced a significant revenue decline due to the COVID-19 pandemic. The company aims to develop a strategic business plan to boost revenue as the economy recovers and restrictions ease.

    - The company seeks to understand the factors that influence the demand for shared bikes in the American market. Specifically, BoomBikes wants to determine:

    - Which variables are significant in predicting the demand for shared bikes.
    - How well these variables explain the fluctuations in bike demand.

    - The company seeks to understand the factors that influence the demand for shared bikes in the American market. Specifically, BoomBikes wants to determine:
        - Which variables are significant in predicting the demand for shared bikes.
        - How well these variables explain the fluctuations in bike demand.

2. **Business Goal**

    - The goal is to develop a predictive model for bike demand using available variables. This model will offer insights into demand dynamics, allowing management to optimize business strategies, meet customer needs, and gain a competitive edge in the market.

3. **Dataset Overview**

    - The dataset includes daily records of bike demand across the American market, capturing various factors such as weather conditions, seasonality, and user behavior. Key columns in the dataset include:

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

4. **Data Understanding and Processing**
   1. Loading the Data
   2. Initial Exploration and Dataset Characteristics
       - Checking for missing or null values, and understanding the distribution of variables
   3. Data Preprocessing
        - Reviewing categorical variables and handling outliers.

5. **Exploratory Data Analysis**
    - Conducted univariate, bivariate, and multivariate analyses using visualizations like histograms, box plots, and correlation matrices to understand relationships between variables.

6. **Feature Engineering**
    - Created dummy variables for categorical features like season, Month, weekday and weather conditions to enable their use in the linear regression model.

7. **Model Building and Feature Selection**

    1. Feature Selection Using Recursive Feature Elimination (RFE)
        - RFE was utilized to identify the most significant features contributing to the predictive power of the model.
    2. Model Development and Comparison
    3. Selecting the Best Model
    4. Final Model
    5. Model Evaluation
        - Residual Analysis
        - Predicting for Test Data

## [Conclusions](https://github.com/vikrant19y/BoomBikes_Demand_Prediction/blob/main/Bike_Renting_Model.ipynb)

1. ***Model Performance***
- The model demonstrates strong performance with the following R-squared scores:
    - **Training Data:** R-squared = **0.8419**
    - **Testing Data:** R-squared = **0.8204**

- This indicates that the model explains approximately **84.2%** of the variance in bike demand on the training set and **82.0%** on the testing set, suggesting that the model generalizes well to unseen data.

2. ***Key Predictors***
- Temperature (`temp`)
    - **Insight:** Temperature is the most significant positive predictor of bike demand.
    - **Coefficient:** **4160.0340**
    - **Impact:** Higher temperatures substantially increase bike demand.

- Year (`year`)
    - **Insight:** There was a significant rise in bike demand in 2019 compared to 2018, reflecting the growing popularity of the service.
    - **Coefficient:** **2007.7272**

- Seasonality (`spring`, `winter`, `Jul`, `Sep`)
    - **Winter:** **Coefficient:** **492.2803** — Increase in demand.
    - **Spring:** **Coefficient:** **-939.9930** — Decrease in demand.
    - **July:** **Coefficient:** **-668.0764** — Decrease in demand.
    - **September:** **Coefficient:** **497.1687** — Increase in demand.
  
- Weather Conditions (`Clear`, `Light_Snow_Rain`)
    - **Clear Weather:** **Coefficient:** **513.9474** — Positive impact on demand.
    - **Light Snow or Rain:** **Coefficient:** **-1663.1473** — Negative impact on demand.

- Day Factors
    - **Working Days:** **Coefficient:** **450.4622** — Higher demand on working days.
    - **Mondays:** **Coefficient:** **536.7014** — Increased demand on Mondays.


## Technologies Used

- Python - Version 3.12
- Pandas - Version 2.2.2
- NumPy - Version 1.26.4
- Matplotlib - Version 3.8.4
- Seaborn - Version 0.13.2
- Scikit-learn - Version 1.2.2
- StatsModel - Version 0.14.0

## Acknowledgements
- This is an assignment done as a part of Executive PG Programme in AI & ML from IIIT, Bangalore  

## Contact

Created by [Vikrant Yadav](https://github.com/vikrant19y) - feel free to contact me!