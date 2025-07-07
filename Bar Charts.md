# Data Visualization Example (s); grouped bar charts
Basic Statistical Analysis

# Vertical Grouped Bar Chart using Titanic Data Set

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

# Horizontal Grouped Bar Chart Using Car Crash Data Set

# Load the Necessary Modules
  import pandas as pd

  import matplotlib.pyplot as plt

  import seaborn as sns

# Load Data Frame
  crashes = sns.load_dataset("car_crashes")

  df = crashes.loc[range(5)]

# Intialize the Figure
f, ax = plt.subplots()

# Plot Total Crashes
  sns.set_color_codes("pastel")

  sns.barplot(x="total", y="abbrev", data=df, label="Total", color="b")

# Plot Crashes Related to Speeding
  sns.set_color_codes("muted")

  sns.barplot(x="speeding", y="abbrev", data=df, label="Speeding-related", color="b")

# Set Title
  plt.title('Speeding-related automobile collisions', fontsize=20)

# Set Legend
  ax.legend(ncol=1, loc="lower right")

  ax.set(xlim=(0, 28), ylabel="State", xlabel="Automobile collisions (per billion miles)")

# saves the image

# plt.savefig("stacked.png")

[(0.0, 28.0),
 Text(0, 0.5, 'State'),
 Text(0.5, 0, 'Automobile collisions (per billion miles)')]
 
 ![image](https://github.com/user-attachments/assets/66a9c684-7304-40f6-b3ba-dab48ab253d1)

 # Data Visualization Example; imported car crash data as a stacked bar chart
Basic Statistical Analysis

# Load the Necessary Modules
    import matplotlib.pyplot as plt

    import seaborn as sns

# Load Dataframe
    crashes = sns.load_dataset("car_crashes")

    df = crashes.loc[range(5)]

# Intialize Figure
f, ax = plt.subplots()

# Plot Total Crashes
    sns.set_color_codes("pastel")

    sns.barplot(x="total", y="abbrev", data=df,
            label="Total", color="b")

# Plot Crashes Related to Speeding
    sns.set_color_codes("muted")

    sns.barplot(x="speeding", y="abbrev", data=df,
            label="Speeding-related", color="b")
# Set Title
plt.title('Speeding-related automobile collisions', fontsize=20)

# Set Legend
    ax.legend(ncol=1, loc="lower right")

    ax.set(xlim=(0, 28), ylabel="State",
       xlabel="Automobile collisions (per billion miles)")

# Save the Image

# plt.savefig("stacked.png")

# Show the Image
  plt.show()

![image](https://github.com/user-attachments/assets/f5b3bbfd-bc8a-44ed-9679-240998d5fbe2)




