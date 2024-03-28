# Classwork 17

## Classwork 1

### Example code from class:
```
penguins = sns.load_dataset("penguins")

# creating pairwise scatterplots of all quantitative variables
sns.pairplot(data=penguins)
plt.show()

# creating pairwise scatterplots of all quantitative variables colored by species
sns.pairplot(data=penguins, hue="species")
plt.show()

# adding a regression line to a scatterplot
sns.lmplot(data=tips, x="total_bill", y="tip", col="time", hue="smoker")
plt.show()

# Create a scatterplot along with distribution plots for the variables
sns.jointplot(data=penguins, x="flipper_length_mm", y="bill_length_mm", hue="species")
plt.show()
```

Documentation for functions:
* `pairplot`: https://seaborn.pydata.org/generated/seaborn.pairplot.html
*  `lmplot`: https://seaborn.pydata.org/generated/seaborn.lmplot.html
* `jointplot`: https://seaborn.pydata.org/generated/seaborn.jointplot.html

### Exercises 

1. **(CW) Create a `pairplot` for the dataset. Which pairs of variables seem most interesting based on this plot? If you color the pair plot by a categorical variable does it reveal any additional information?**
1. **(CW) Create a plot of with a regression line between two quantitative variables you just identified. Does it look like the two variables have a linear relationship?**
1. **(CW) Create a `jointplot` between these two variables. Color by a categorical variable. What extra information does the jointplot provide?**
1. Explore different jointplot "kinds" : `"scatter", "kde", "hist", "reg"`. Which kind is most appropriate for your data?

## Classwork 2
The goodreads data set can be downloaded at this link: https://drive.google.com/file/d/1h8mKao45AnBW5FZkx4b34Lo2jwGjBasH/view?usp=sharing 

Each row corresponds to one book. Column definitions are the following:

Variable | Description
--|--
`Name` | The title of the book
`RatingDist1` | The number of 1-star ratings
`RatingDist2` | The number of 2-star ratings
`RatingDist3` | The number of 3-star ratings
`RatingDist4` | The number of 4-star ratings
`RatingDist5` | The number of 5-star ratings
`RatingDistTotal` | The total number of ratings
`pagesNumber` | The number of pages in the book
`PublishDay` | The day of the month the book was published
`PublishMonth` | The month the book was published (1-12)
`Publisher` | The publisher of the book
`CountsOfReview` | The number of reviews the book has received (different from ratings)
`PublishYear` | The year the book was published
`Language` | The language the book is written in
`Authors` | The author(s) of the book
`Rating` | The average rating given to this book (out of 5)

**(CW) Brainstorm questions to guide your exploratory analysis of this data.**

What might lead to an interesting discovery?
What are you curious about given the dataset columns we have access to?

## Classwork 3

### Code from class

```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Stops columns from being cut off when displayed
pd.set_option('display.max_colwidth', None)

# log-scale axis
sns.relplot(data = books, x = "RatingDistTotal", y = "CountsOfReview")
plt.xscale("log")
plt.yscale("log")
plt.show()

books.sort_values("Rating")
books.sort_values(["Rating", "PublishYear"])
books.sort_values(["Rating", "PublishYear"], ascending = False)
```

### Exercises

1. **(CW) What is the title of the book with the greatest number of pages?**
1. What is the title of the book with the greatest number of ratings?
1. What is the title of the book with the greatest number of reviews?
1. **(CW) Sort the data by “PublishYear”, “PublishDay”, and “RatingDistTotal” in descending order.**


## Classwork 4

### Code from class

```
books = books[(books["PublishDay"] > 10) & (books["PublishDay"] < 20)]

books = books[(books["Publisher"] == "HarperCollins") | (books["Publisher"] == "Penguin Books") | (books["Publisher"] == "Simon  Schuster")]
books = books[books["Publisher"].isin(["Harper Collins", "Penguin Books", "Simon  Schuster"])]
```

### Exercises

1. **(CW) Filter your dataframe to remove outliers from the “PublishYear” variable, and save the dataframe.**
1. **(CW) Filter your dataframe based on the “Language” variable: Choose only three languages to include.**
1. Filter books to only rows for which “pagesNumber” is greater than 0 and less than 20,000 and save as `books`.
1. Are there other columns it would make sense to filter on to clean up the data? Perform more filtering as you see fit.

## Classwork 6

### Code from class

```
books["RatingsPlusReviews"] = books["RatingDistTotal"] + books["CountsOfReviews"]	
books["fracRated1"] = books["RatingDist1"]/books["RatingDistTotal"]
books["Rated5MinusRated1"] = books["RatingDist5"] - books["RatingDist1"]
```

### Exercises


1. Assign a column called ”FracRated5” that’s the fraction of the total ratings (”RatingDistTotal”) that are equal to 5 (”RatingDist5”)
1. What happens when you add two columns containing strings? Try adding the ”Authors” and ”Name” columns.
1. Create a new column of your choosing.
1. Assign a column called ”OneFiveRating” that’s equal to the average rating for the book if only 1-star and 5-star ratings are considered

## Classwork 7

1. Assign a new variable called “Season” based on the “PublishMonth” column. Let “Season”  be defined as follows:
      * “Season” equals “Winter”  if “PublishMonth”  equals 1, 2, or 3
      * “Season”  equals “Spring”  if “PublishMonth” equals 4, 5, or 6
      * “Season”  equals “Summer” if “PublishMonth” equals 7, 8, or 9
      * “Season”  equals “Fall”  if “PublishMonth” equals 10, 11, or 12
1.  Define the following columns:
      * “TimePeriod” based on the “PublishYear” column, with at least 4 categories.
      * “Popularity” based on the “RatingDistTotal” column, with at least 3 categories. 
