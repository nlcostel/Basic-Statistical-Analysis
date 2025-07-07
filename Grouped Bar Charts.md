# Data Visualization Example; grouped bar charts using Titanic dataset
Basic Statistical Analysis

# Import Packages
  import pandas as pd

  import matplotlib.pyplot as plt

  import seaborn as sns

# Import the Titanic Dataset
  titanic = pd.read_csv("titanic.csv")

# Set the Style of the Bar Charts
  sns.set_theme(style="whitegrid", color_codes=True)

# Set Title
  plt.title('Titanic survivors and deaths by class', fontsize=20)

# Generate a Vertical Bar Chart
  sns.countplot(x="class", hue="survived", color="b", data=titanic)

# Save the Image

# plt.savefig("groupedbarchart.png")

# Shows the Image

  plt.show()

![image](https://github.com/user-attachments/assets/33b4364f-dcf5-42f4-a714-da76ac595160)
