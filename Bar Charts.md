# Data Visualization Example (s); Bar Charts
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

 

 # Stacked Bar Chart Using Car Crash Data Set

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



# Vertical Vs. Horizontal Bar Charts
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


# Data Visualization Example; Histograms
Basic Statistical Analysis

# Load packages
  import pandas as pd

  import matplotlib.pyplot as plt

# Load data
  heights = pd.read_csv("height.csv")

# Plot histogram
  fig, ax = plt.subplots()

  plt.hist(heights['Height'], bins=6)

  ax.set_xlabel('Height')

  ax.set_ylabel('Frequency')

# plt.savefig('histogram6.png')
plt.show()
  
![image](https://github.com/user-attachments/assets/56d2acdf-06b0-45ba-bc6d-e8c3b7d82f46)

  fig, ax = plt.subplots()

# Plotting with more bins
  plt.hist(heights['Height'], bins=10)

  ax.set_xlabel('Height')
  
  ax.set_ylabel('Frequency')

  plt.show()

![image](https://github.com/user-attachments/assets/c73f1061-0118-4bbb-bc34-597694ff5c85)

