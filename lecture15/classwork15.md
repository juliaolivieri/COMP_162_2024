# Classwork 15

Mapping between R and Python commands: https://github.com/juliaolivieri/COMP_162_2024/blob/main/lecture15/python_R_translation.md

Dataset used in class examples:`taxis.csv`, https://drive.google.com/file/d/1yzcou-mgYXhanO_gP69TZyEC_2S5sm0f/view?usp=sharing

## Part 1

### Reading and writing data

#### Code from class

```
# read dataframe
pd.read_csv("taxis.csv")

# write dataframe
taxis.to_csv("new_taxis.csv", index = False)
```

#### Exercises

1. **(CW) Import the required packages for these exercises:**
   ```
   import matplotlib.pyplot as plt
   import pandas as pd
   import seaborn as sns
   ```
1. Load `penguins.csv` into your notebook using `pd.read_csv()`. Save the dataframe to a variable called `penguins`. Link to dataset: https://drive.google.com/file/d/1ESxaIakPh6IpsA_x1H1798003CuqJP8r/view?usp=sharing 
2. Load `mining.csv` into your notebook. Save this dataframe to a variable called `mining`. Link to dataset: https://drive.google.com/file/d/1Z6_ejcVUrmB39BO3GJ2bmwD8lrrX2TvW/view?usp=sharing 

### Descriptive statistics

#### Code from class

```
# find number of rows and columns
taxis.shape

# display first 10 rows
taxis.head(10)

# display last 8 rows
taxis.tail(8)

# Output summary information about column types
taxis.info()

# Output summary statistics for each column
taxis.describe(include = "all")

# Find the frequency of each value of a categorical column
taxis["payment"].value_counts()
```

#### Exercises

### Indexing

#### Code from class

```
# create dataframe
animals = pd.DataFrame.from_dict({"species" : ["dog", "cat", "penguin"], 
                                  "size" : [40, 10, 80], 
                                  "name" : ["Typo", "Ralph", "Pinky"], 
                                  "age" : [5, 18, 12]})

# two ways to index into the same value
animals.iloc[0,0]
animals.loc[3, "species"]

# two ways to index into the same value
animals.iloc[0:2, 1:4]
animals.loc[[3, 6],["size", "name", "age"]]
```

#### Exercises

## Part 2

### Filtering and sorting

#### Code from class

```
# subset to selected columns
taxis[[“fare”, “payment”, “pickup_zone”, “pickup_borough”]]

# subset to only rows for which the color is green
taxis[taxis[“color”] == “green”]

# subset to only rows for which the fare is less than 5
taxis[taxis[“fare”] < 5]

# sort dataframe by fare
taxis.sort_values("fare")
```

#### Exercises

### Plotting

#### Code from class

```
# create a histogram for fare
sns.displot(data = taxis, x = "fare")
plt.plot()

# create a bar plot for pickup_borough
sns.displot(data = taxis, x = "pickup_borough")
plt.plot()
```

#### Exercises
