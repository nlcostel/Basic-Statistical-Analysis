# Descriptive Statistics
Basic Statistical Analysis

# nump.mean()function
import numpy as np

# Creates an array
  arr1 = np.array([4, 8, 2, 10, 5])

# Prints the mean 
  print(np.mean(arr1))

# Output= 5.8

# Finding the mean of a column in a data frame

  import pandas as pd

  scores = pd.read_csv('ExamScores.csv')

# Prints the first few lines of data
  print(scores.head())

# Prints the mean for each exam
  print(scores.mean())

# Prints the mean for Exam1 only
  print(scores[['Exam1']].mean())

# Prints the means for Exam1 and Exam2
  print(scores[['Exam1', 'Exam2']].mean())

   Exam1  Exam2  Exam3  Exam4
   
0    100     66     74     68

1     76     84    100     75

2     89     80    100     95

3     83     76     91     74

4     86     99     78     78

Exam1    82.70

Exam2    79.40

Exam3    73.34

Exam4    76.50

dtype: float64

Exam1    82.7

dtype: float64

Exam1    82.7

Exam2    79.4

dtype: float64

# nump.median() function

  import numpy as np

# Creates an array
  arr1 = np.array([4, 8, 2, 10, 5])

# Prints the median
  print(np.median(arr1))

# Output= 5.0

# DataFrame.median() function

  import pandas as pd

# Loads the ExamScores dataset
  scores = pd.read_csv('ExamScores.csv')

# Prints the median for each exam
  print(scores.median())

# Prints the median for Exam1 only
  print(scores[['Exam1']].median())

Load default template...

  import pandas as pd

# Loads the ExamScores dataset
  scores = pd.read_csv('ExamScores.csv')

# Prints the median for each exam
  print(scores.median())

Run

Program executed

Exam1    83.0

Exam2    79.5

Exam3    74.5

Exam4    75.0

dtype: float64

Exam1    83.0

dtype: float64

# scipy.stats.mode() function

  import numpy as np
  
  import scipy.stats as st

# Creates an array
  arr1 = np.array([[4, 8, 2], [2, 5, 10], [2, 1, 10]])

  print(arr1)

# Prints the mode
print(st.mode(arr1, keepdims=True))

[[ 4  8  2]

 [ 2  5 10]
 
 [ 2  1 10]]
 
ModeResult(mode=array([[ 2,  1, 10]]), count=array([[2, 1, 2]]))

# numpy.mode()function

  import pandas as pd

# Loads the ExamScores dataset
  scores = pd.read_csv('ExamScores.csv')

# Prints the mode(s) for each exam
  print(scores.mode())

# Prints the mode(s) for Exam1 only
  print(scores[['Exam1']].mode())

    Exam1  Exam2  Exam3  Exam4
    
0     78   84.0  100.0   74.0

1     83  100.0    NaN   75.0

2     89    NaN    NaN    NaN

   Exam1
   
0     78

1     83

2     89

# Mean & Median
The rent dataset lists the monthly rent (in USD) of 
 apartments with area less than 1000 ft ^ 2 in 6 cities. The columns of the dataset give the rents in Santa Monica, CA, Boise, ID, Tucson, AZ, Detroit, MI, Pittsburgh, PA, and Orlando, FL
  
  import pandas as pd

  rent = pd.read_csv('rent.csv')

  print(rent)

# The mean rent for Santa Monica is found as follows
  print(rent['Santa Monica CA'].mean())

# The mean rent for all cities is found as follows
  print(rent.mean())

# The median rent for all cities is found as follows
  print(rent.median())

Run

Program executed

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

7929.5

Santa Monica CA    7929.5

  Boise ID         1078.4
  
  Tucson AZ        1789.5
  
  Detroit MI       2096.5
  
  Pittsburgh PA    2344.1
  
  Orlando FL       1825.9
  
dtype: float64

Santa Monica CA    8125.0

  Boise ID          965.0
  
  Tucson AZ        1625.0
  
  Detroit MI       2085.0
  
  Pittsburgh PA    2318.0
  
  Orlando FL       1782.5
  
dtype: float64
