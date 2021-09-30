# Data_602

## Problem Statement
Trip duration is the most fundamental measure in all modes of transportation. Hence, it is crucial to predict the trip-time precisely for the advancement of Intelligent 
Transport Systems (ITS) and traveller information systems. Data mining techniques are employed in this paper to predict the trip duration of rental bikes in Seoul Bike sharing system. The rental duration prediction needs to be carried out with the combination of Seoul Bike data and weather data.

## About the Data
The Data used include trip duration, trip distance, pickup-dropoff latitude and longitude, temperature, precipitation, wind speed, humidity, solar radiation, snowfall, 
ground temperature and 1-hour average dust concentration.

# https://www.kaggle.com/saurabhshahane/seoul-bike-trip-duration-prediction

Due to system limitations I could only access 1.5 million records out of 9.6 million records and performed EDA on it.

## Observations
In the given dataset there are 2 types of data. They are numerical and categorical. The columns Pmonth, Pday, Phour, Pmin, PDweek, Dmonth, Dday, Dhour, Dmin, DDweek are categorical and the columns Duration, Distance, Haversine, Temp, Precip, Wind, Humid, Solar, Snow, GroundTemp, Dust are numerical.

The duration column is in minutes and the distance column is in meters.

The Duration, Distance, Haversine are right-skewed and Temp, Wind, Humid, GroundTemp have a normal distribution.

Based on the insights from various graphs it looks like people who rent the bikes are using them to travel to offices(jobs).
