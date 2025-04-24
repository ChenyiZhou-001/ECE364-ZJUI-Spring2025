# Metro Interstate Traffic Volume Prediction

## Overview
Predict hourly traffic volume on a major highway using past traffic and weather data.

## Dataset
- **Link**:
- **Train set**: From 2012-10-02 09:00:00 to 2017-05-17 20:00:00 (33742)
- **Val set**: From2017-05-17 20:00:00 to 2018-01-25 18:00:00 (7231)
- **Test set**: From 2018-01-25 19:00:00 to 2018-09-30 23:00:00 (7231)
  
Each record includes:
- `date_time`: Timestamp
- `temp`, `rain_1h`, `snow_1h`, `clouds_all`: Weather features
- `holiday`, `weather_main`, `weather_description`: Categorical context
- `traffic_volume`: Target variable (vehicles/hour)

## Task
- Train a time series regression model on the train set.
- Validate the trained model on the val set.
- Test the best model on the test set.

- Use past 24 hours as context input (or engineered features)  

During the testing phase, the model will predict using a sliding window. Specifically, to predict the traffic volume for a given hour t in the test set, you need to use the feature data from the last 24 hours preceding it (i.e., from time t-24 to t-1) as the model's input.

## Requirements
- < 15 million parameters
- Use Linear Regression, MLPs, or LSTMs
- Pytorch, Scikit-learn
  
## Evaluation metric: 
- Mean Absolute Error (MAE)

## Output Format
Id,Predicted_Volume  

37251, 85.3  

37252, 97.2  

...





