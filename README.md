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

## Data Dictionary

| Column Name     | Modeling Role  | Measurement Level | Description                                                                                     |  
|-----------------|----------------|-------------------|-------------------------------------------------------------------------------------------------|
| PU_ct	          | Dependent	     | Ratio	           | Represents the count of bike pickups; used as a response variable in regression models.         |  
| DO_ct	          | Dependent	     | Ratio	           | Represents the count of bike drop-offs; used as a response variable in regression models.       |  
| temp	          | Independent	   | Interval	         | Temperature in degrees Celsius; used to predict bike usage based on weather conditions.         |  
| precip	        | Independent	   | Ratio	           | Precipitation in millimeters; used to assess the impact of rain on bike usage.                  |  
| windspeed	      | Independent	   | Ratio	           | Wind speed in kilometers per hour; considered to study its effect on biking comfort and safety. |  
| uvindex	        | Independent	   | Ordinal	         | UV index, categorized from low to high; used to determine the impact of sun exposure on biking. |  
| icon	          | Independent	   | Nominal	         | Weather condition icon (e.g., sunny, cloudy, rain); used to categorize daily weather visually.  |  

### Differences Between Training and Test Data
- The training data includes the target variables (Number of Pick ups (PO_ct)) and (Number of Drop-offs (DO_ct)) and the independent variables ('temp','precip','windspeed','uvindex' & 'icon'), allowing us to train and evaluate the model, while the test data, based on the split (40%), is used solely for generating predictions to assess model performance on unseen data.
- Task 1-7 for PO_ct using all the independent variables and Task 8 is for DO_ct using all the independent variables.

## Model Details
### Architecture  
- This model card utilizes only linear model such as **Linear Regression**.

### Evaluation Metrics  
- MSE (Mean Square Error): Measures the model's ability to distinguish the optimal feature combination for predicting PU_ct and DO_ct separately, our target variables, involves the use of five features in different combinations. This configuration yields the lowest mean squared error (MSE) on the test data for different combination of features.

### Final Values of MSEs for All Data using 'linear regression' model:

| Dataset                                           |       MSE         |   
|---------------------------------------------------|-------------------|  
| Training MSE of training data using one feature   | 64.63185358976104 |  
| Test MSE of test data using one feature           | 71.53543417972891 |   
| Training MSE of training data using two features  | 61.454167225797   |  
| Test MSE of test data using two features          | 65.02373285537077 |  
| Training MSE of training data using three features| 61.4322641173538  |  
| Test MSE of test data using three features        | 65.3813722910624  |  
| Training MSE of training data using four features | 52.58457605801069 |  
| Test MSE of test data using four features         | 48.38692187059774 |  
| Training MSE of training data using five features | 45.62027690029117 |  
| Test MSE of test data using five features         | 59.659317806457906|  

### Software Used to Implement the Model
- **Software:** Python (with libraries such as Pandas, Scikit-learn, seaborn & matplotlib)

### Version of the Modeling Software: 
- **'pandas'**: '2.2.2',
- **'scikit-learn'**: '1.4.2',
- **'seaborn'**: '0.13.2',
- **'matplotlib'**: '3.8.4**

## Quantitative Analysis



