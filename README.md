# DC Bikeshare Weather Impact Analysis using Linear Regression

This GitHub repository analyzes the impact of weather on bike-sharing in Washington, D.C., using linear regression models to predict bike usage based on weather variables like temperature and precipitation. It includes data preparation, model building, and visualization scripts.

## Basic Information
**Names:** N M Emran Hussain  
**Email:** nmemranhussain2023@gmail.com  
**Date:** January 2025  
**Model Version:** 1.0.0  
**License:** [MIT License](LICENSE)

## Intended Use
**Purpose:** This GitHub repository analyzes the impact of weather on bike-sharing in Washington, D.C., using linear regression models to predict bike usage based on variables like temperature and precipitation. It includes data preparation, model building, and visualization scripts, aimed at guiding operational and strategic decisions in urban planning.
**Intended Users:** Data Analysts, Data scientists, machine learning enthusiasts, educators.  
**Out-of-scope Uses:** The model is not intended for production use in any critical applications or real-time decision-making systems.

## Training Data
**Dataset Name:** Capital Bikeshare Data ('202402-capitalbikeshare-tripdata.csv', '202403-capitalbikeshare-tripdata.csv', '202404-capitalbikeshare-tripdata.csv' & 'DC_weather_2024.csv')
**Number of Samples:** 318689, 436947, 490266 & 367   
**Features Used:** 'temp','precip','windspeed','uvindex'&'icon'
**Data Source:** [capitalbikeshare-data](https://s3.amazonaws.com/capitalbikeshare-data/index.html)

### Splitting the Data for logistic regression model
The dataset was divided into training and validation data as follows:
- **Training Data Split:** 60%
- **Validation Data Split:** 40%

### Data Dictionary

| Column Name     | Modeling Role  | Measurement Level | Description                                                                                     |
| PU_ct	          | Dependent	     | Ratio	           | Represents the count of bike pickups; used as a response variable in regression models.         |
| DO_ct	          | Dependent	     | Ratio	           | Represents the count of bike drop-offs; used as a response variable in regression models.       |
| temp	          | Independent	   | Interval	         | Temperature in degrees Celsius; used to predict bike usage based on weather conditions.         |
| precip	        | Independent	   | Ratio	           | Precipitation in millimeters; used to assess the impact of rain on bike usage.                  |
| windspeed	      | Independent	   | Ratio	           | Wind speed in kilometers per hour; considered to study its effect on biking comfort and safety. |
| uvindex	        | Independent	   | Ordinal	         | UV index, categorized from low to high; used to determine the impact of sun exposure on biking. |
| icon	          | Independent	   | Nominal	         | Weather condition icon (e.g., sunny, cloudy, rain); used to categorize daily weather visually.  |

