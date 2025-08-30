In this project, New York Taxi dataset will be analyzed through data manipulation, transformation, cleaning, feature selection and data processing with multiple tools in SQL and Python. The source of dataset is Kaggle and the dataset can be found [here](https://www.kaggle.com/datasets/microize/nyc-taxi-dataset). Dataset range from 2019 until 2019 with daily trips ducumentations from 4 different type of taxis, which are:
1. Yellow taxi. Data range from January 2009 until September 2023.
2. Green taxi. Data range from January 2014 until September 2023.
3. For Hire Vehicle. Data range from January 2015 until September 2023.
4. High volume for Hire Vehicle. Data range from January 2019 until September 2023.

Based on features that available on each type of data, there some interesting topics will be explored:
1. Predict whether a consument will give tips aor no tips. This can be done through classification prediction.
2. Predict wheter a consument will give a big tips, normal tips or no tips at all.
3. Predict anomaly of customers who give a big tips.
4. Predict the amont cost of service from customer. This can be done with regression.
5. Forecasting of customer throught daily dataset with time series data analysis.

# 1. Data Manipulation
Various steps in data manipulations are:

1. Convert data New York Yellow Taxi in 2019, where the previous format is in csv to parquet file type. This step follows the Polars code in [here](https://github.com/imdwipayana/Portfolio-Projects/blob/main/67%20GB%20Full%20Data%20Analysis/Convert_csv_2019_to_parquet.ipynb).
2. fafd
