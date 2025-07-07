# Data Visualization Example; Pie Charts
Basic Statistical Analysis

# Load the Necessary Libraries
  import matplotlib.pyplot as plt
  
  import seaborn as sns

# Load the Titanic Dataset
  df = sns.load_dataset("titanic")

# Count the Number of Passengers for Each Class
  a = df[df.pclass == 1]["pclass"].count()

  b = df[df.pclass == 2]["pclass"].count()

  c = df[df.pclass == 3]["pclass"].count()

# Data to Plot
  labels = 'First', 'Second', 'Third'

  sizes = [a, b, c]

# Define Lot
  plt.pie(sizes, labels=labels, autopct='%1.1f%%')

# Set Title
  plt.title('Titanic passengers by class', fontsize=20)

# Set Legend
  patches, texts = plt.pie(sizes)

  plt.legend(patches, labels, loc="lower right")

# Set Axes to be Equal to Produce a Perfectly Circular Chart
  plt.axis('equal')

# Save the Image
# plt.savefig("piechart.png")

# Show the Image
  plt.show()

![image](https://github.com/user-attachments/assets/692ef11c-f803-4dc7-9d85-3f34bd476a55)

# Make a Pie Chart with Counts Instead of Percentages
  tot = sum(sizes)

  def autopct(x): return "%d" % round(x*tot/100, 2)


  plt.pie(sizes, labels=labels, autopct=autopct);

![image](https://github.com/user-attachments/assets/23d6dd39-efc1-4828-a9a4-60dba69c490b)

# Create Exploded Pie Chart


# Load Necessary Packages
  import matplotlib.pyplot as plt

  import seaborn as sns

# Load the Titanic Dataset
  df = sns.load_dataset("titanic")

# Calculate the Number in Each Class
  a = df[df.survived == 1]["survived"].count()

  b = df[df.survived == 0]["survived"].count()

# Create a Tuple of the Categories
  explodeTuple = (0.1, 0.0)

# Define Data to Plot
  labels = 'Survived', 'Did not survive'

  sizes = [a, b]

# Define Plot
  plt.pie(sizes, labels=labels, autopct='%1.1f%%', explode=explodeTuple)

# Set Title
  plt.title('Survivors of the Titanic', fontsize=20)

# Set Axes to be Equal to Produce a Perfectly Circular Chart
  plt.axis('equal')

# Save the Image

# plt.savefig("explodedpiechart.png")

# Show the Image
  plt.show()

![image](https://github.com/user-attachments/assets/469570d5-a7e5-4509-afaf-dd9f86e1b90f)

