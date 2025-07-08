# Descriptive Statistics; Measures of Variability
Basic Statistical Analysis

# std() and var()
  import numpy as np

  arr1 = np.array([10, 2, 5, 7, 3, 5])

# Population standard deviation for the array
  print(np.std(arr1))

# Population variance of the array
  print(np.var(arr1))

# Sample standard deviation for the array
  print(np.std(arr1, ddof=1))

# Sample variance of the array
  print(np.var(arr1, ddof=1))

2.6246692913372707

6.88888888888889

2.8751811537130436

8.26666666666667

# Finding standard deviation of a column in a data frame

  import pandas as pd

# Loads the ExamScores dataset
  scores = pd.read_csv('ExamScores.csv')

# Sample standard deviation for each exam
  print(scores.std())

# Sample standard deviation for Exam1 only
  print(scores[['Exam1']].std()) 

# Sample variance for each exam
  print(scores.var())

# Sample variance for Exam1 only
  print(scores[['Exam1']].var())

# Population variance for each exam
  print(scores.var(ddof=0))

# Sample variance for Exam1 only
  print(scores[['Exam1']].var(ddof=0))


import pandas as pd

# Loads the ExamScores dataset
scores = pd.read_csv('ExamScores.csv')

# Sample standard deviation for each exam
print(scores.std())



 

Run

Program executed

Exam1     9.291756

Exam2    14.332780

Exam3    21.754296

Exam4     8.056560

dtype: float64

Exam1    9.291756

dtype: float64

Exam1     86.336735

Exam2    205.428571

Exam3    473.249388

Exam4     64.908163

dtype: float64

Exam1    86.336735

dtype: float64

Exam1     84.6100

Exam2    201.3200

Exam3    463.7844

Exam4     63.6100

dtype: float64

Exam1    84.61

dtype: float64

# Standard deviation and variance
  import pandas as pd
  rent = pd.read_csv('rent.csv')
  print(rent)

# The standard deviation in rent for all cities is found as follows.
  print(rent.std())

# The variance in rent for all cities is found as follows.
  print(rent.var())

   Santa Monica CA    Boise ID  ...    Pittsburgh PA    Orlando FL
   
0            10230        1600  ...             2480          2242

1            10000        1500  ...             2435          2000

2             9000        1029  ...             2405          1912

3             8500        1025  ...             2350          1895

4             8250         980  ...             2320          1800

5             8000         950  ...             2316          1765

6             7000         950  ...             2305          1685

7             6500         925  ...             2290          1670

8             6000         925  ...             2275          1665

9             5815         900  ...             2265          1625

[10 rows x 6 columns]

Santa Monica CA    1572.680744

  Boise ID          253.125002
  
  Tucson AZ         363.153243
  
  Detroit MI        664.308538
  
  Pittsburgh PA      72.520419
  
  Orlando FL        191.608658
  
dtype: float64

Santa Monica CA    2.473325e+06

  Boise ID         6.407227e+04
  
  Tucson AZ        1.318803e+05
  
  Detroit MI       4.413058e+05
  
  Pittsburgh PA    5.259211e+03
  
  Orlando FL       3.671388e+04
  
dtype: float64

# mad()

  import pandas as pd

# Loads the ExamScores dataset
  scores = pd.read_csv('ExamScores.csv')

# Prints the mean absolute deviation of all scores
  print(scores.mad())

# Prints the mean absolute deviation of Exam 1
  print(scores['Exam1'].mad())

Run

Program executed

Exam1     7.1360

Exam2    12.1200

Exam3    17.7928

Exam4     5.7000

dtype: float64

7.135999999999999



