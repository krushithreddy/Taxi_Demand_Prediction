# Taxi_Demand_Prediction
Predict demand for yellow taxis in New York City

Data source
http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml

Problem type
Time series prediction/regression

Divide NYC into regions and time values into pickup bins
Divide the time into bins of 10 minutes
Use KMeans clustering to divide the city of New York into regions based on pickup density of 2015 values and average intercluster distance

Feature extraction for time series prediction
Use jan, feb, march 2016 filled data (missing values filled with zeros) to extract exponentially weighted moving averges of past values
One hot encode days of week
Take pickup bin value one week earlier as a feature
Take pickup bin value one day earlier as a feature
Take last 5 pickup bin values as 5 features
Take max, min of last 5 pickup values as 2 features
Take std dev of last 10 values as 1 feature
Take 120 point DFT of pickup values in last 2 hours i.e. 120 bins
## Score
0.004 MAPE
