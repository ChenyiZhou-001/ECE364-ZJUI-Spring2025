# PM2.5 Concentration Forecasting (Beijing)

## Overview
Forecast PM2.5 concentration one hour ahead using past weather and pollution data.

## Dataset
- **Link**: https://drive.google.com/drive/folders/1m3kaWZ1sytYor7I2CJ2rI-jLV1rayzLF?usp=sharing
- **Train set**: From 2010-01-01-0 to 2013-07-02-3 (30676)
- **Val set**: From 2013-07-02-04 to 2014-04-02-01 (6574)
- **Test set**: From 2014-04-02-02 to 2014-12-31-23 (6575)
  
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

- Predict PM2.5 using a sliding window of **5 past hours**

During the testing phase, the model will predict using a sliding window. Specifically, to predict the PM2.5 value for a given hour `t` in the test set, you need to use the feature data from the last five hours preceding it (i.e., from time `t-5` to `t-1`) as the model's input.
Note that when predicting the very first time point (t_start) in the test set, the required input for the model (data from time t_start-5 to t_start-1) will actually be the last five data points from the validation set.

## Requirements
- < 15 million parameters
- Use Linear Regression, MLPs, or LSTMs
- Pytorch, Scikit-learn
  
## Evaluation metric: 
- Mean Absolute Error (MAE)

## Output Format
Id,Predicted_PM2.5  

37251, 85.3  

37252, 97.2  

...




