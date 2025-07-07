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

