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
The goodreads data set can be downloaded at this link: https://drive.google.com/file/d/1Oqs4GN01e35_6BAfrEPYbfGvUC7ARR5p/view?usp=sharing

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

## Importing code from class

```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Stops columns from being cut off when displayed
pd.set_option('display.max_colwidth', None)
```

## Sorting code from class

```
books.sort_values("Rating")
books.sort_values(["Rating", "PublishYear"])
books.sort_values(["Rating", "PublishYear"], ascending = False)
```

## Filtering code from class

```
books = books[(books["PublishYear"] > 1800) & (books["PublishYear"] < 2024)]
books = books[(books["Language"] == "eng") | (books["Language"] == "en-US") | (books["Language"] == "en-GB") | (books["Language"] == "en-CA")]
```

## Creating a new column code from class

```
books["RatingsPlusReviews"] = books["RatingDistTotal"] + books["CountsOfReviews"]	
books["fracRated1"] = books["RatingDist1"]/books["RatingDistTotal"]
books["Rated5MinusRated1"] = books["RatingDist5"] - books["RatingDist1"]
