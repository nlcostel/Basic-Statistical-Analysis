# Data Visualization Example; imported unemployment rates & line graph
Basic Statistical Analysis

# Import the Necessary Libraries
  import pandas as pd
  
  import matplotlib.pyplot as plt

# Loads the Unemployment Dataset
  unemployment = pd.read_csv("unemployment.csv")

# Set Title
  plt.title('U.S. unemployment rate', fontsize=20)

# Set x and y Axis Labels
  plt.xlabel('Year')
  
  plt.ylabel('% of total labor force')

# Make Plot
  plt.plot(unemployment["Year"], unemployment["Value"])

# Show the Image
  plt.show()
  
![image](https://github.com/user-attachments/assets/6d5c13a6-dce2-4a20-b055-d7d01caff70d)
