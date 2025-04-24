# PM2.5 Concentration Forecasting (Beijing)

## Overview
Forecast PM2.5 concentration one hour ahead using past weather and pollution data.

## Dataset
- **Link**: XXX
- **Train set**: 
- **Val set**: 
- **Test set**: 

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



