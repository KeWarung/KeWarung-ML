# KeWarung-ML
**PRODUCT SALES PREDICTION**

**GENERAL DESCRIPTION**

Production sales prediction feature was initiated based on the store owners who experienced stock shortages during periods of high demand. Such periods should be an opportunity to increase sales profits. However, the uncertainty of the type of product and the timing of the increase in demand often leads to insufficient stock to meet the demand. By analyzing historical sales data, market trends, and other factors, KeWarung can provide predictions of which products are likely to sell well in the future.

We used Tensorflow library in Python for making Timeseries model. In this case, we used product sales dataset from UCI Machine Learning Repository to predict the upcoming week (next 7 days) of each product in that store. Then, for each product we compared the weekly prediction data with current available stock in inventory. The product that have sales prediction number greater than the available stock in inventory will input to a list of recommended product for restocking, and we also provided estimated quantity of each recommended product that must be restocked


**DATASET**

This dataset consist sales data from a retail store range in year 2010-2011.
https://docs.google.com/spreadsheets/d/1lHZh9LdKABQZyfnuegDW73s_T3UUzsPk/edit?usp=sharing&ouid=114221394866737468360&rtpof=true&sd=true 


**LAUNCH**

We preprocessed the dataset and build model in model_script_w30.ipynb 

The fixed model is saved as model_script_w30.h5

Then we defined prediction function that will receive the input data from database, preprocess data, make prediction, and postprocess data in prediction_script.py


**API ENDPOINT**

We used flask library in python to make an endpoint for this machine learning model in app.py to receive input in csv format and give output in json format

DEPENDENCIES

All the dependencies required for the project was stored in requirements.txt
