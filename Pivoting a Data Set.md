# Pivoting a Data Set
Basic Statistical Analysis

# Loads the Pandas Library
import pandas as pd

# Creates a Data Frame
df = pd.DataFrame({                  
                   'Student': {0: "Michael", 1: "Arushi", 2: "Roberta", 3: "Michael", 4: "Arushi", 5: "Roberta"},
                   'Score': {0: 90, 1: 98, 2: 92, 3: 90, 4: 98, 5: 92}, 
                   'Date': {0: "2018-01-03", 1: "2018-01-03", 2: "2018-01-03", 3: "2018-01-13", 
                            4: "2018-01-13", 5: "2018-01-13"}}, 
                  columns=['Date','Student','Score'])
                  
print("Original data frame:\n", df)

print("\n Pivot() output: \n", pd.pivot(df, index = "Date", columns = "Student", values= "Score"))

# Original data frame:

          Date  Student  Score
          
0  2018-01-03  Michael     90

1  2018-01-03   Arushi     98

2  2018-01-03  Roberta     92

3  2018-01-13  Michael     90

4  2018-01-13   Arushi     98

5  2018-01-13  Roberta     92

 # Pivot() output: 
 
 Student     Arushi  Michael  Roberta
 
Date         

2018-01-03      98       90       92

2018-01-13      98       90       92
