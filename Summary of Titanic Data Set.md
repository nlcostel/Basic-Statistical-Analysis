# Summary of Imported Titanic Data Set
Basic Statistical Analysis

# Loads the Pandas Library
import pandas as pd

# Loads the Titanic Dataset 
titanic = pd.read_csv('titanic.csv')

# Find the Number of Rows and Columns
print(titanic.shape)

# Find the Column Names
print(titanic.columns)

# Find the Data Types of the Columns
print(titanic.dtypes)

# Find Median for All Numeric Variables
print(titanic.median(numeric_only=True))

Run

Program executed

(891, 15)

Index(['survived', 'pclass', 'sex', 'age', 'sibsp', 'parch', 'fare',
       'embarked', 'class', 'who', 'adult_male', 'deck', 'embark_town',
       'alive', 'alone'],
      dtype='object')
      
survived         int64

pclass           int64

sex             object

age            float64

sibsp            int64

parch            int64

fare           float64

embarked        object

class           object

who             object

adult_male        bool

deck            object

embark_town     object

alive           object

alone             bool

dtype: object

survived       0.0000

pclass         3.0000

age           28.0000

sibsp          0.0000

parch          0.0000

fare          14.4542

adult_male     1.0000

alone          1.0000

dtype: float64
