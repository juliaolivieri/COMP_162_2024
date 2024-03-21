# Classwork 15

Mapping between R and Python commands: https://github.com/juliaolivieri/COMP_162_2024/blob/main/lecture15/python_R_translation.md

`mining.csv`: https://drive.google.com/file/d/1Z6_ejcVUrmB39BO3GJ2bmwD8lrrX2TvW/view?usp=sharing

`taxis.csv`: https://drive.google.com/file/d/1yzcou-mgYXhanO_gP69TZyEC_2S5sm0f/view?usp=sharing

`penguins.csv`: https://drive.google.com/file/d/1ESxaIakPh6IpsA_x1H1798003CuqJP8r/view?usp=sharing 

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
1. 

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

```

# two ways to index into the same value
animals.iloc[0,0]
animals.loc[3, "species"]
```

#### Code from class

#### Exercises

## Part 2

### Filtering and sorting

#### Code from class

#### Exercises

### Plotting

#### Code from class

#### Exercises
