# Step 1: preparing the data set

# This module will be used to prepare a pandas dataframe and calculate descriptive statistics
  import pandas as pd

# input your data in the Python list below. 

# For example, if your temperature data is:  81, 79, 80, 85, 83, 85, 87, 84, 84, 88, 85, 87

# then the step below should be set as:   temperatures = [81, 79, 80, 85, 83, 85, 87, 84, 84, 88, 85, 87]
  temperatures = [91,90,90,91,91,93,93,93,91,90,88,88,88,90]

# prepare a dataframe for temperatures.
  temperatures_df = pd.DataFrame(temperatures, columns=['temperature'])

# print temperatures dataframe
  print(temperatures_df)

    temperature
    
0            91

1            90

2            90

3            91

4            91

5            93

6            93

7            93

8            91

9            90

10           88

11           88

12           88

13           90

# Step 2: calculating descriptive statistics

# Pandas dataframe has several methods that calculate descriptive statistics. 

# mean
mean = temperatures_df['temperature'].mean()

print("Mean=", round(mean,2))

# median
median = temperatures_df['temperature'].median()

print("Median=", round(median,2))

# variance
variance = temperatures_df['temperature'].var()

print("Variance=", round(variance,2))

# standard deviation
stdeviation = temperatures_df['temperature'].std()

print("Standard Deviation=", round(stdeviation,2))

# describe - a useful function that calculates several different descriptive statistics
statistics = temperatures_df['temperature'].describe()

print("")

print ("Describe method")

print (statistics)

Mean= 90.5

Median= 90.5

Variance= 3.04

Standard Deviation= 1.74

Describe method

count    14.000000

mean     90.500000

std       1.743118

min      88.000000

25%      90.000000

50%      90.500000

75%      91.000000

max      93.000000

Name: temperature, dtype: float64

# Step 3: line graph to display trend

import matplotlib.pyplot as plt

# line chart
plt.plot(temperatures_df['temperature']) # plot

# setting a title for the plot, x-axis and y-axis
plt.title('Line plot of temperature data', fontsize=20) 

plt.xlabel('day')

plt.ylabel('temperature')

# show the plot
plt.show()

![image](https://github.com/user-attachments/assets/0f776c7b-7fa7-4dc6-9beb-1e85652eeeed)

# Step 4: side-by-side boxplots to compare distributions

import matplotlib.pyplot as plt

import seaborn as sns

import numpy as np

import random

# creates temperature data for Zion. You don't need to know how this data is created. 

# The temperature data created for Zion will be unique to you. 
mean = random.randint(temperatures_df['temperature'].min(),temperatures_df['temperature'].max())

std_deviation = random.randint(round(temperatures_df['temperature'].std(),0),round(2*temperatures_df['temperature'].std(),0))

zion_temperatures = np.random.normal(mean, std_deviation, 25)

zion_temperatures = pd.DataFrame(zion_temperatures, columns=['temperature'])

# side-by-side boxplots require the two dataframes to be concatenated and require a variable identifying the data
temperatures_df['id'] = 'my_data'

zion_temperatures['id'] = 'zion_data'

both_temp_df = pd.concat((temperatures_df, zion_temperatures))

# sets a title for the plot, x-axis, and y-axis
plt.title('Boxplot for comparison', fontsize=20) 

# prepares the boxplot
sns.boxplot(x="id",y="temperature",data=both_temp_df)

# shows the plot
plt.show()

![image](https://github.com/user-attachments/assets/f62b6d88-be73-4ef8-9489-ddb908033b85)

# IN SUMMARY

My data set shows 14 days of daily maximum temperature readings from my city. 
temperature = [91, 90, 90, 91, 91, 93, 93, 93, 91, 90, 88, 88, 88, 88, 90]
The statistics below suggest that the distribution is relatively symmetrical 
and tightly clustered around the mean. Since the mean and median are equal, 
the data does not appear to be skewed. The standard deviation is relatively low 
which means temperatures are consistently close to average. This indicates a 
low variability with fairly stable temperatures and with no extreme outliers. 

Mean: 90.5

Median: 90.5

Variance: 3.04

Standard Deviation: 1.74

The line graph best shows the general trend; it allowed me to 
visualize slight fluctuations across the 14 days and see how temperatures rose and fell.
Despite small ups and downs, the graph revealed that most days remained within a 5-degree range. 
 
Measures of central tendency (mean, median) help us understand the “typical” 
or average value in the data set. Measures of variability (variance, standard deviation) 
tell us how spread out the data is around the average. Together these metrics provide a 
more complete picture of the distribution, and how consistent (or inconsistent) the data 
is across the set. This can be crucial when determining trends or predicting future values. 
The box plot was most helpful in comparing my city’s data to Zion’s. 
It visually showed differences in range, median, and variability. My city had narrower interquartile range
and a median of 90.5 suggesting consistent temperatures. Zion’s data likely had a wider spread,
or more variation, meaning its temperatures fluctuated more during the same time period. 
 


