# New York Taxi: The 67GB Data Analysis

In this project, New York Taxi dataset will be analyzed through data manipulation, transformation, cleaning, feature selection and data processing with multiple tools in SQL and Python. The source of dataset is Kaggle and the dataset can be found [here](https://www.kaggle.com/datasets/microize/nyc-taxi-dataset). Dataset range from 2019 until 2019 with daily trips ducumentations from 4 different type of taxis, which are:
1. Yellow taxi. Data range from January 2009 until September 2023.
2. Green taxi. Data range from January 2014 until September 2023.
3. For Hire Vehicle. Data range from January 2015 until September 2023.
4. High volume for Hire Vehicle. Data range from January 2019 until September 2023.

Based on features that available on each type of data, there some interesting topics will be explored:
1. Predict whether a consument will give tips aor no tips. This can be done through classification prediction.
2. Predict wheter a consument will give a big tips, normal tips or no tips at all.
3. Predict anomaly of customers who give a big tips.
4. Try to do clustering.
5. Predict the amont cost of service from customer. This can be done with regression.
6. Forecasting of customer throught daily dataset with time series data analysis.

## 1. Data Manipulation
Various steps in data manipulations are:

1. Convert data New York Yellow Taxi in 2019, where the previous format is in csv to parquet file type. This step follows the Polars code in [here](https://github.com/imdwipayana/Portfolio-Projects/blob/main/67%20GB%20Full%20Data%20Analysis/Convert_csv_2019_to_parquet.ipynb).
2. Select feature data that avalilable in all of the monthly file data. Here data from For Hire Vehicle match only 2 features to other type of taxis. For that reason, data from this taxi is not included in the analysis. From around 15 features, the selected features that matching with other taxi types are:
   
   a. Pick up time.
   
   b. Drop off time
   
   c. Number of passengers
   
   d. Distance
   
   e. Payment type
   
   f. Tips amount
   
   g. Cost of trip
   
4. Transform the format of data type pick up dan drop off columns from string to date time format.
6. Deleting data that less meaningful such as negative distance and distance that more than 50 miles (there are some taxis serve more than 100000 miles). Here, it is assumed that the maximum service distance is 50 miles.
7. Deleting data that has negative distance, negative tips amount and negative cost of trip.
8. Deleting data which serive is more than 24 hours (counted from the difference of drop off and pick up time).

Considering the size of data, there will be step by step analysis from a chunk of dataset to find the pattern about how to analyze the dataset appropriately. Here is the step on analyzing the dataset:
1. Try one month of data on January 2009 from Ney York Yellow Taxi. The Python analysis can be found [here](https://github.com/imdwipayana/Portfolio-Projects/blob/main/67%20GB%20Full%20Data%20Analysis/yellow%20taxi%20january%202009.ipynb).
2. Add more monthly dataset until all data in 2009 are included.
3. Then add all year of New York Yellow Taxi dataset from 2009 until 20023.
4. Then add dataset from different taxi such as Green Taxi and High Volume for Hire Taxi. The data manipulation can be foun in [here](https://github.com/imdwipayana/Portfolio-Projects/blob/main/67%20GB%20Full%20Data%20Analysis/Data%20Manipulation%20New%20York%20Taxi%20Tip%20Prediction.ipynb)
5. Transformation to Time Series data can be found [here](https://github.com/imdwipayana/Portfolio-Projects/blob/main/67%20GB%20Full%20Data%20Analysis/new_york_taxi_time_series.ipynb)


