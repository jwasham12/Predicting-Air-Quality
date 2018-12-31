## Problem Statement

Using the past climate and PM2.5 data in Beijing, build an accurate classification model in order to give alerts to citizen of Beijing to take the necessary health caution.

## Executive Summary

Due to the rapid growth of economics and urbanization, air quality problem catches both government and public’s eyes, especially in some most populated and industrialized cities such as Beijing. Beijing, the capital of the People’s Republic of China and the world’s second most populous city, is known for air pollution and constantly batting against widespread health problems caused by air pollution. To help the citizen of Beijing with this issue, we decided to make a statistical prediction model based on the past climate and PM2.5 data in order to give alerts to the citizen of Beijing. The alerts will advise the citizens to take the necessary health caution.

## Data Description

- pm_data.csv from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Beijing+PM2.5+Data)

|Feature|Type|Description|
|---|---|---|
|No|numeric|Row number| 
|Year|numeric|Year of the record| 
|Month|numeric|Month of the record|
|Day|numeric|Day of the record| 
|Hour|numeric|Hour of the record| 
|PM2.5|numeric|PM2.5 concentration (ug/m^3)|
|DEWP|numeric|Dew Point| 
|TEMP|numeric|Temperature|
|PRES|numeric|Pressure|
|CBWD|categorical|Combined wind direction| 
|LWS|numeric|Cumulated wind speed (m/s)|
|LS|numeric|Cumulated hours of snow|
|LR|numeric|Cumulated hours of rain|

## Method

- Check and clean the data
- Research different PM2.5 levels
- Classify PM2.5 levels
- Build models using cross validation
- Select the best model
- Interpret the model

## Result

|Model|Train Accuracy|Test Accuracy|
|---|---|---|
|Logistic Regression|0.7363|0.7399| 
|KNN (scale)|0.7747|0.7824|
|Random Forest|0.7971|0.8030| 
|Boosting (GBM)|0.7733|0.7782|

## Conclusion

Overall, the cross-validated random forest model with 5 randomly selected predictors (mtry = 5) had the best accuracy of predicting the PM2.5 level based on the climate data. We also check variable importance and found that dew point is the most influencing variable in predicting the PM2.5 level. In addition, the variable importance shows that the cumulated hours of snow variable is not influencing the prediction.
