# Task18
Description
Identify missing values in a dataset and practice handling them using Pandas techniques such as dropping and filling missing values.
Objective
Understand missing values as a common data-preprocessing problem and learn how to detect and handle them.
Tools Used
Python
Pandas
Jupyter Notebook
Tasks Performed
Loaded a dataset using Pandas.
Checked for missing values using isna().
Counted missing values in each column using isna().sum().
Used notna() to identify available values.
Compared two approaches for handling missing data:
Dropping: Remove rows or columns containing missing values with dropna().
Filling: Replace missing values with suitable values using fillna().
Used the mean or median carefully to fill missing numerical values.
Created a cleaned version of the dataset.
Important Pandas Functions
Function         Purpose
isna()         Identifies missing values notna()        Identifies non-missing values isna().sum()   Counts missing values in each column dropna()       Removes rows or columns with missing values fillna()       Replaces missing values
Example Code
import pandas as pd

# Load the dataset
df = pd.read_csv("data.csv")

# Display missing-value counts
print(df.isna().sum())

# Display non-missing values
print(df.notna())

# Fill missing numerical values with the column mean
df["Age"] = df["Age"].fillna(df["Age"].mean())

# Remove rows that still contain missing values, if appropriate
cleaned_df = df.dropna()

# Save the cleaned dataset
cleaned_df.to_csv("cleaned_data.csv", index=False)
Note: Replace data.csv and Age with the actual dataset filename and column name. Choose dropna() or fillna() based on the dataset and the meaning of the missing data.
Suggested Datasets
Titanic Dataset
House Prices Dataset
Outcome
Learned how to detect missing values, compare dropping and filling methods, and prepare a cleaner dataset for further analysis.
