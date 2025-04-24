# PM2.5 Concentration Forecasting (Beijing)

## Overview
Forecast PM2.5 concentration one hour ahead using past weather and pollution data.

## Dataset
- **Link**: XXX

The dataset includes the following features (Missing values should be handled appropriately (e.g., interpolation)):
- `pm2.5`: PM2.5 concentration (target)
- `DEWP`: Dew point
- `TEMP`: Temperature
- `PRES`: Atmospheric pressure
- `cbwd`: Wind direction (categorical), you may use wind direction (`cbwd`) by one-hot encoding or discard it
- `Iws`: Cumulative wind speed
- `Is`: Cumulative hours of snow
- `Ir`: Cumulative hours of rain
- Timestamps: `year`, `month`, `day`, `hour`

## Task
- Train a time series regression model on the train set.
- Validate the trained model on the val set.
- Test the best model on the test set.

- Predict PM2.5 using a sliding window of 5 past hours

## Requirements
- < 15 million parameters
- Use Linear Regression, MLPs, or LSTMs
- Pytorch, Scikit-learn
  
## Evaluation metric: 
- Mean Absolute Error (MAE)

## Output Format
Id,Predicted_PM2.5  

0, 85.3  

1, 97.2  

...

- `Id`: Row number of the test set (starting from 0)  
- `Predicted_PM2.5`: Model's predicted value for that hour



