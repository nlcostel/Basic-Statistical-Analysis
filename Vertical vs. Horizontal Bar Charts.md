# Data Visualization Example; vertical vs. horizontal bar charts
Basic Statistical Analysis

# Loads the Necessary Modules
  import pandas as pd

  import matplotlib.pyplot as plt

  import seaborn as sns

# Loads the Titanic Dataset
  titanic = pd.read_csv("titanic.csv")

# Sets the Style of the Bar Charts
  sns.set_theme(style="whitegrid", color_codes=True)

# Title
  plt.title('Titanic passengers by class', fontsize=20)

# Plots a Vertical Bar Chart
  sns.countplot(x="class", color="b", data=titanic)

# Saves the Image

# plt.savefig("verticalbarchart.png")

# Shows the Image
  plt.show()

![image](https://github.com/user-attachments/assets/41184305-273e-4900-aa23-abfc919a89ca)

# Plots a Horizontal Bar Chart
  sns.countplot(y="class", color="b", data=titanic)
  
<AxesSubplot: xlabel='count', ylabel='class'>

![image](https://github.com/user-attachments/assets/6ef17fe7-a615-4360-90cb-5079fd91f112)
