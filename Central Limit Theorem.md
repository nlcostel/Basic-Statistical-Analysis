# Step 1: generating population data

import pandas as pd

import matplotlib.pyplot as plt

import numpy as np

import scipy.stats as st

# use gamma distribution to randomly generate 500 observations. 
shape, scale = 1.95, 2.5

tpcp = 100*np.random.gamma(shape, scale, 500)

# pandas library can be used to convert the array into a dataframe of rounded figures with the column name TPCP.
tpcp_df = pd.DataFrame(tpcp, columns=['TPCP'])

tpcp_df = tpcp_df.round(0)

# print the dataframe to see the first 5 and last 5 observations (note that the index of dataframe starts at 0).
print("TPCP data frame\n")

print(tpcp_df)

TPCP data frame

      TPCP
0    425.0
1    175.0
2    996.0
3    263.0
4    146.0
..     ...
495  271.0
496   85.0
497  148.0
498  317.0
499  452.0

[500 rows x 1 columns]

# Step 2: creating a histogram plot of population data

# create a figure for the plot. 
fig, ax = plt.subplots()

# create a histogram plot with 50 bins of TPCP population data. 
plt.hist(tpcp_df['TPCP'], bins=50)

# set a title for the plot, x-axis, and y-axis.
plt.title('TPCP population distribution', fontsize=20)

ax.set_xlabel('TPCP')

ax.set_ylabel('Frequency')

# show the plot.
plt.show()

![image](https://github.com/user-attachments/assets/9e51a696-78f1-4f54-b29b-5f991ae32493)

# Step 3: calculating the population mean

# You can use the "mean" method of a pandas dataframe.
pop_mean = tpcp_df['TPCP'].mean()

print("Population mean =", round(pop_mean,2))

Population mean = 508.98

# Step 4: drawing one random sample from the population data and calculating the sample mean

# use sample method of the dataframe to select a random sample, with replacement, of size 50.
tpcp_sample_df = tpcp_df.sample(50, replace=True)

# print the sample mean.
sample_mean = tpcp_sample_df['TPCP'].mean()

print("Sample mean =", round(sample_mean,2))

Sample mean = 501.16

# Step 5: repeatedly drawing samples and saving the sample mean for each sample

# run a for loop to repeat the process Step 4 one thousand times to select one thousand samples.

# save the mean of each sample that was drawn in a Python list called means_list.
means_list = []

for i in range(1000):

    tpcp_sample_df = tpcp_df.sample(50, replace=True)
    
    sample_mean = tpcp_sample_df['TPCP'].mean()
    
    means_list.append(sample_mean)
    
# create a Python dataframe of means.
means_df = pd.DataFrame(means_list, columns=['means'])

print("Dataframe of 1000 sample means\n")

print(means_df)

Dataframe of 1000 sample means

      means
      
0    608.82

1    498.08

2    435.58

3    534.08

4    542.78

..      ...

995  513.40

996  535.72

997  500.98

998  655.46

999  472.70

[1000 rows x 1 columns]

# Step 6: creating a histogram plot of the sample means from Step #5

# create a figure for the plot. 
fig, ax = plt.subplots()

# create a histogram plot with 50 bins of 1,000 means. 
plt.hist(means_df['means'], bins=50)

# set a title for the plot, x-axis and y-axis.
plt.title('Distribution of 1000 sample means', fontsize=20) # title

ax.set_xlabel('Means')

ax.set_ylabel('Frequency')

# show the plot.
plt.show()

![image](https://github.com/user-attachments/assets/4e143bfd-ceea-484e-94a7-24a80ff99fd8)

# Step 7: mean and the standard deviation of the sample mean distribution

# calculate mean of the 1,000 sample means (this is called the grand mean or mean of the means).
mean1000 = means_df['means'].mean()

print("Grand Mean (Mean of 1000 sample means) =",round(mean1000,2))

# calculate standard deviation of the 1,000 sample means.
std1000 = means_df['means'].std()

print("Std Deviation of 1000 sample means =",round(std1000,2))

# print the probability that a specific mean is 450 or less for a Normal distribution with mean and standard deviation of 1,000 sample means.
prob_450_less_or_equal = st.norm.cdf(450, mean1000, std1000)

print("Probability that a specific mean is 450 or less =", round(prob_450_less_or_equal,4))

Grand Mean (Mean of 1000 sample means) = 508.69

Std Deviation of 1000 sample means = 54.5

Probability that a specific mean is 450 or less = 0.1408

# IN SUMMARY

Mean of the TPCP population data: 508.98

Mean of random sample (n=50): 501.16

50 random values of the population had an average very close to the population mean, 
showing that a sufficient sample can produce a representation for the estimated population mean. So yes, this was a good match. 
By selecting 1,000 random samples and storing their means we created a Data Frame 
(1,000 different groups of 50 random values). 
This output supports the central limit theorem by showing how the distribution of the sample means behaves. 
The distribution of the 1,000 means does approximate a normal distribution (bell-shaped curve), 
even though the population may not be perfectly normal. 
This further confirms the central limit theorem, which states that sampling distribution of the sample mean
approaches normality as the number of samples increases.

Grand mean: 508.69

Standard deviation of the sample means: 54.5 

The grand mean is also very close to the population mean. 
This confirms the second part of the central limit theorem, 
which states the average of many sample averages will be close to the real average, and the spread will be smaller. 


