# Descriptive Statistics; discrete probability distributions
Basic Statistical Analysis

# Mean, variance, and standard dev. of a discrete random variable

  from scipy.stats import rv_discrete

# Defines a list containing the outcomes in the sample space
  x = [0,1,2,3,4,5,6]

# Defines a list containing the probabilities for each outcome
  p = [0.1,0.2,0.3,0.1,0.1,0.0,0.2]

# Links the values in x to the probabilities in p
  discvar = rv_discrete(values=(x,p))

# To find the mean, the .mean() method is used.

# Returns the mean of the discrete random variable
  print(discvar.mean())

# To find the variance, the .var() method is used.

# Returns the variance of the discrete random variable 
  print(discvar.var())

# To find the standard deviation, the .std() method is used.

# Returns the standard deviation of the discrete random variable
  print(discvar.std())

2.7
3.8099999999999987
1.9519221295943132

# Z-score; earnings surprise

  import pandas as pd

# Create a DataFrame containing the eps data
  earnings_surprise = pd.DataFrame([11.36, 7.89, 1.96, 0, -3.12, -9.52])

  print(earnings_surprise.mean())

  print(earnings_surprise.std())

# Compute z-score
  print((11.36-earnings_surprise.mean())/earnings_surprise.std())

  0    1.428333
  
dtype: float64

0    7.526849

dtype: float64

0    1.319499

dtype: float64

# norm.cdf() and norm.sf()

import scipy.stats as st

# For a normal distribution, if the mean is 0 

# and the standard deviation is 1, 

# what is P(z <= -0.25)?
  print(st.norm.cdf(-0.25, 0, 1))

# For a normal distribution, if the mean is 0 

# and the standard deviation is 1,

# what is P(z <= 1.5)?
  print(st.norm.cdf(1.5, 0, 1))

# For a normal distribution, if the mean is 0

# and the standard deviation is 1, 

# what is P(z >= -0.25)?
  print(st.norm.sf(-0.25, 0, 1))

# For a normal distribution, if the mean is 0 

# and the standard deviation is 1, 

# what is P(z >= 1.5)?
  print(st.norm.sf(1.5, 0, 1))

# To find the probability between two values, the

# difference between the two probabilities is calculated.

# For a normal distribution, if the mean is 0 

# and the standard deviation is 1, 
  #what is P(-0.25 <= z <= 1.5)?
  print(st.norm.cdf(1.5, 0, 1) - st.norm.cdf(-0.25, 0, 1))

# For a normal distribution, if the mean is 0   

# and the standard deviation is 1, 

# what is P(1.5 <= z <= 2.85)?
  print(st.norm.cdf(2.85, 0, 1) - st.norm.cdf(1.5, 0, 1))

# Both norm.cdf() and norm.sf() can also be 

# used for non-standard normal distributions,

# that is, when the mean is not 0  or the 

# standard deviation is not 1.

# For a normal distribution, if the mean is 55

# and the standard deviation is 7.5, 

# what is P(x <= 62)?
  print(st.norm.cdf(62, 55, 7.5))

# For a normal distribution, if the mean is 55

# and the standard deviation is 7.5, 

# what is P(x >= 51)?

  print(st.norm.sf(51, 55, 7.5))

# For a normal distribution, if the mean is 55 

# and the standard deviation is 7.5, 

# what is P(49 <= x <= 60)?
  print(st.norm.cdf(60, 55, 7.5) - st.norm.cdf(49, 55, 7.5))



# For a normal distribution, if the mean is 55 
# and the standard deviation is 7.5, 
# what is P(49 <= x <= 60)?
print(st.norm.cdf(60, 55, 7.5) - st.norm.cdf(49, 55, 7.5))

Run

Program executed

0.4012936743170763

0.9331927987311419

0.5987063256829237

0.06680720126885807

0.5318991244140656

0.06462123981394485

0.8246760551477705

0.7030985713961488

0.5356520638696805

# norm.ppf() and norm.isf()

import scipy.stats as st

# For a normal distribution, if the mean is 0 and 

# the standard deviation is 1, what is z* if P(z < z*) = 0.135?
  print(st.norm.ppf(0.135, 0, 1))

# For a normal distribution, if the mean is 0 and 

# the standard deviation is 1, what is z* if P(z > z*) = 0.405?
  print(st.norm.isf(0.405, 0, 1))

# Both norm.ppf() and norm.isf() can also be used with non-standard normal distributions.

# For a normal distribution, if the mean is 55 and 

# the standard deviation is 7.5, what is x* if P(x < x*) = 0.8247?
  print(st.norm.ppf(0.8247, 55, 7.5))

# For a normal distribution, if the mean is 55 and 

# the standard deviation is 7.5, what is x* if P(x > x*) = 0.95?
  print(st.norm.isf(0.95, 55, 7.5))

  late...
print(st.norm.ppf(0.8247, 55, 7.5))

# For a normal distribution, if the mean is 55 and 
# the standard deviation is 7.5, what is x* if P(x > x*) = 0.95?
print(st.norm.isf(0.95, 55, 7.5))

Run

Program executed

-1.1030625561995975

0.2404260311423079

62.00069589151078

42.66359779786396

# t.cdf() and t.sf()

import scipy.stats as st

# For a t-distribution, if the degrees of freedom is 30, the mean is 0,
# and the standard deviation is 1, what is P(t < -0.25)?
  print(st.t.cdf(-0.25, 30, 0, 1))

# For a t-distribution, if the degrees of freedom is 30, the mean is 0,
# and the standard deviation is 1, what is P(t < 1.5)?
  print(st.t.cdf(1.5, 30, 0, 1))

# For a t-distribution, if the degrees of freedom is 30, the mean is 0,
# and the standard deviation is 1, what is P(t > -0.25)?
  print(st.t.sf(-0.25, 30, 0, 1))

# For a t-distribution, if the degrees of freedom is 30, the mean is 0,
# and the standard deviation is 1, what is P(t > 1.5)?
  print(st.t.sf(1.5, 30, 0, 1))

# To find the probability between two critical values, 
# the difference between the two probabilities is calculated.
# For a t-distribution, if the degrees of freedom is 30, the mean is 0,
# and the standard deviation is 1, what is P(-0.25 < t < 1.5)?
  print(st.t.cdf(1.5, 30, 0, 1) - st.t.cdf(-0.25, 30, 0, 1))

# For a t-distribution, if the degrees of freedom is 30, the mean is 0,
# and the standard deviation is 1, what is P(1.5 < t < 2.85)?
  print(st.t.cdf(2.85, 30, 0, 1) - st.t.cdf(1.5, 30, 0, 1))

# Both t.cdf() and t.sf() can also be used for t-distributions 
# with different degrees of freedom and when the mean is 
# not 0 or the standard deviation is not 1.
# For a t-distribution, if the degrees of freedom is 59, the mean is 55,
# and the standard deviation is 7.5, what is P(t < 62)?
  print(st.t.cdf(62, 59, 55, 7.5))

# For a t-distribution, if the degrees of freedom is 34, the mean is 55,
# and the standard deviation is 7.5, what is P(t > 51)?
  print(st.t.sf(51, 34, 55, 7.5))

# For a t-distribution, if the degrees of freedom is 59, the mean is 55,
# and the standard deviation is 7.5, what is P(49 < t < 60)?
  print(st.t.cdf(60, 59, 55, 7.5) - st.t.cdf(49, 59, 55, 7.5))

0.40214570454028753

0.927967035435677

0.5978542954597125

0.07203296456432302

0.5258213308953895

0.06811767651326017

0.8227740421098456

0.7013638496128232

0.5327479742680783

# t.ppf() and t.isf()

  import scipy.stats as st

# For a t-distribution, if the degrees of freedom is 49, the mean is 0 and 
# the standard deviation is 1, what is t* if P(t < t*) = 0.135?
  print(st.t.ppf(0.135, 49, 0, 1))

# For a t-distribution, if the degrees of freedom is 49, the mean is 0 and 
# the standard deviation is 1, what is t* if P(t > t*) = 0.405?
  print(st.t.isf(0.405, 49, 0, 1))

# Both t.ppf() and t.isf() can also be used with non-standard t-distributions.
# For a t-distribution, if the degrees of freedom is 24, the mean is 55 and 
# the standard deviation is 7.5, what is t* if P(t < t*) = 0.8247?
  print(st.t.ppf(0.8247, 24, 55, 7.5))

# For a t-distribution, if the degrees of freedom is 24, the mean is 55 and 
# the standard deviation is 7.5, what is t* if P(t > t*) = 0.95?
  print(st.t.isf(0.95, 24, 55, 7.5))
  
-1.1156820266358158

0.2417276381058361

62.13980379235694

42.168384400679294

# f.cdf() and f.sf()

  import scipy.stats as st

# For an F-distribution, if the degrees of freedom between samples is 2
# and the degrees of freedom within samples is 5, what is P(F < 2)?
  print(st.f.cdf(2, 2, 5))

# f.sf(f, dfb, dfw) returns the probability of  being greater than a critical value f for an -distribution with  equal to dfb and  equal to dfw.
# For an F-distribution, if the degrees of freedom between samples is 2
# and the degrees of freedom within samples is 5, what is P(F > 3.5)?
  print(st.f.sf(3.5, 2, 5))

# To find the probability between two critical values, the difference between the two probabilities is calculated.
# For an F-distribution, if the degrees of freedom between samples is 2
# and the degrees of freedom within samples is 5, what is P(2 < F < 3)?
  print(st.f.cdf(3, 2, 5) - st.f.cdf(2, 2, 5))

0.7699518541666883

0.11206549034164981

0.09075065358884016

# Chi-square distribution, finding areas and percentiles

  from scipy.stats import chi2

# Defines the degrees of freedom and chi-square_0
  df = 7
  
  x2 =  1.689

# chi2.cdf can be used to calculate the area under the curve between 0 and chi-square_0.
# Calculates the area under the curve between 0 and chi-square_0
  area = chi2.cdf(x2, df)
  
  print(area)

# Conversely, if the area is defined, chi2.ppf gives the chi-square_0 value, or percentile, necessary to obtain that area.
# Defines an area under the curve
  a = 0.025
  
# Calculates the percentile
  perc = chi2.ppf(a, df)

0.02496315095256541

# finding probability

  from scipy.stats import chi2

  df = 7
  
  x2 = 3.111

  area = chi2.cdf(x2, df)

  print(area)

  0.12545259857860666

  # finding percentiles

  from scipy.stats import chi2

  df = 5
  
  a = 0.95

  perc = chi2.ppf(a, df)

  print(perc)

  11.070497693516351
