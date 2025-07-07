# Data Visualization Example; scatter plot
Basic Statistical Analysis

# Load the necessary libraries
  import matplotlib.pyplot as plt
  import seaborn as sns

  import numpy as np

  import pandas as pd

# Create the data points
  x = np.array([0, 5, 3, 4, 7, 8, 10])

  y = np.array([5, 2, 5, 15, 27, 15, 31])

# Define the plot
  sns.regplot(x=x, y=y, ci=None)

# Save the image

# plt.savefig("scatterplot.png")

# Show the image
  plt.show()

![image](https://github.com/user-attachments/assets/eb0d91bc-10fe-49ea-8147-0e2f9d2af838)

# Load the rock data set
  df = pd.read_csv("rock.csv")

# Set title
  plt.title('Area and perimeter of rock', fontsize=20)

# define plot
  sns.regplot(x=df["Area"], y=df["Perimeter"], ci=None, fit_reg=False)

# show the image
  plt.show()

![image](https://github.com/user-attachments/assets/d7868071-c473-4aa0-8fde-8a4b1aedfc7c)
