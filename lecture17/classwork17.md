# Classwork 17

Example code from class:
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


1. **(CW) Create a `pairplot` for the dataset. Which pairs of variables seem most interesting based on this plot? If you color the pair plot by a categorical variable does it reveal any additional information?**
1. **(CW) Create a plot of with a regression line between two quantitative variables you just identified. Does it look like the two variables have a linear relationship?**
1. **(CW) Create a `jointplot` between these two variables. Color by a categorical variable. What extra information does the jointplot provide?**
1. Explore different jointplot "kinds" : `"scatter", "kde", "hist", "reg"`. Which kind is most appropriate for your data?
