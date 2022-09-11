# Project---Airbnb-analysis
This project is related to Seattle airbnb case study part of Udacity - Nano degree data scientist program
For this project 2 CSV files has been used:
Calendar.csv - including listing id and the price and availability for that day
and listings.csv - including full descriptions and average review score

Purpose of this project: Since 2008, guests and hosts have used Airbnb to travel in a more unique, personalized way. As part of the Airbnb Inside initiative, this dataset describes the listing activity of homestays in Seattle, WA
These millions of listings generate a lot of data, which can be analysed and used for a variety of purposes, including security, business decisions, understanding customer and provider (host) behaviour and performance on the platform, guiding marketing initiatives, and implementing innovative additional services, among others.

4 business questions:
1.Comparison of average price on weekend vs weekday.
2.Monthly and yearly trend of average price.
3.Correlation of review_scores_rating,property_type,room_type,bedrooms with the price of listings.
4.Factors impacting Price through Linear Regression model technique.

Libraries used for this project:
# Useful packages
import numpy as np
import pandas as pd
import seaborn as sns
from collections import Counter
import matplotlib.pyplot as plt 
plt.rc("font", size=14)
import time as tm
from datetime import datetime
import operator
from sklearn import preprocessing
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error
from sklearn.metrics import accuracy_score
from sklearn.model_selection import train_test_split
from sklearn.metrics import classification_report
from sklearn.metrics import confusion_matrix
from sklearn.utils import resample
from sklearn.preprocessing import minmax_scale
from sklearn.preprocessing import StandardScaler

Reading CSV files:
for first 2 business questions 
data_c = pd.read_csv("calendar.csv", encoding='latin-1', low_memory=False)
data_c.head()

For last 2 business questions
data_l = pd.read_csv("listings.csv", encoding='latin-1', low_memory=False)
data_l.head()

Solution:
it can be seen that if review score rating, review per month score and number of reviews are increased price would decrease whereas there is not much impact of bedroom and beds on price, however if longitude and latitude is increasing then price will also increase, they are directly correlated 
Also prices are high for 6 bedroom house and house boat entire bedroom



