# Data Visualization Example; Box Plots
Basic Statistical Analysis

# Loads the necessary libraries
  import matplotlib.pyplot as plt

  import seaborn as sns

  import pandas as pd

# Loads the ExamScores dataset
  scores = pd.read_csv("ExamScores.csv")

# Transforms the data
  df = pd.melt(scores, value_name="Score", var_name="Exam")

# Plot
  sns.boxplot(x="Exam", y="Score", data=df)

# Saves the image

# plt.savefig("Examsboxplots.png")

# Shows the image
  plt.show()

![image](https://github.com/user-attachments/assets/1cd74e91-1b26-45a7-9377-d6b5142ecd97)

# Plots without outliers
  sns.boxplot(x="Exam", y="Score", data=df, whis=(0,100));

![image](https://github.com/user-attachments/assets/817568f4-56dc-4fb3-b946-eec3711b407f)

# Loads packages
  import seaborn as sns

  import pandas as pd

  import matplotlib.pyplot as plt

# Reads the mtcars.csv file into a dataframe called mtcars
  mtcars = pd.read_csv("mtcars.csv")

# Prints the first few lines of mtcars

  print(mtcars.head())

          Unnamed: 0   mpg  cyl   disp   hp  drat     wt   qsec  vs  am  gear  \
          
0          Mazda RX4  21.0    6  160.0  110  3.90  2.620  16.46   0   1     4   

1      Mazda RX4 Wag  21.0    6  160.0  110  3.90  2.875  17.02   0   1     4  

2         Datsun 710  22.8    4  108.0   93  3.85  2.320  18.61   1   1     4   

3     Hornet 4 Drive  21.4    6  258.0  110  3.08  3.215  19.44   1   0     3  

4  Hornet Sportabout  18.7    8  360.0  175  3.15  3.440  17.02   0   0     3   


   carb  
   
0     4  

1     4  

2     1  

3     1  

4     2  

# Show summary statistics for the variable wt

  mtcars.wt.describe()

count    32.000000

mean      3.217250

std       0.978457

min       1.513000

25%       2.581250

50%       3.325000

75%       3.610000

max       5.424000

Name: wt, dtype: float64

# Plots a box plot
  sns.boxplot(data=mtcars.wt, width=0.35, whis=1.5);

![image](https://github.com/user-attachments/assets/50074244-ef91-4f26-a931-8cabd60b7930)

