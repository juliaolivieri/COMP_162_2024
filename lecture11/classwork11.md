# Classwork 11

## Part 1: Data visualization

### Code from class
```
# creating a histogram visualization
bike_sharing %>%
  ggplot(aes(temperature_F, fill=season)) +
  geom_histogram()

# creating a freqpoly visualization
bike_sharing %>%
  ggplot(aes(temperature_F, color=season)) +
  geom_freqpoly()

# creating a density visualization
bike_sharing %>%
  ggplot(aes(temperature_F, color=season)) +
  geom_density()

# sorting box plot by mean temperature
bike_sharing %>%
  ggplot(aes(reorder(month, temperature_F), temperature_F)) +
  geom_boxplot()
```

### Exercises
1. **(CW) Load the bike sharing data from last class (https://github.com/juliaolivieri/COMP_162_2024/blob/main/lecture10/classwork10.md).**
1. **(CW) Create a plot of `windspeed` by `season`. Try using `geom_freqpoly()`, `geom_density()`, and `geom_histogram()`. Which visualization do you prefer?**
1. **(CW) Create a box plot of `season` vs `count`. Sort the boxes.**
1. Create a box plot of `windspeed` by `season`. Choose another categorical variable to set `fill` to.
1. Create a `geom_line()` plot of `temperature_F` vs `date_noyear`. Add smoothing with `geom_smooth()`. Were there big temperature differences between the two years?
1. Create a plot of `humidity` by `month`. Try using `geom_freqpoly()`, `geom_density()`, and `geom_histogram()`. Which visualization do you prefer?
1. Try adding points to the plot above with `geom_jitter()`. Do you prefer the plot with or without these points?
1. Create a box plot of `humidity` by `month`. Choose a variable to set `fill` to.
1. Create a `geom_line()` plot of `temperature_F` vs `date_noyear`. Add smoothing with `geom_smooth()`. Were there big temperature differences between the two years?

## Part 2: Correlation

### Code from class:
```
# calculate the correlation between the count and temperature_F columns of bike_sharing
cor.test(bike_sharing$count, bike_sharing$temperature_F)

# calculate the pairwise correlations between temperature_F, humidity, windspeed, and count
cor(select(bike_sharing, temperature_F, humidity, windspeed, count))

# Create every pairwise scatterplot between temperature_F, humidity, windspeed, and count
pairs(select(bike_sharing, temperature_F, humidity, windspeed, count))
```

| Variable | Description |
| -- | -- |
| `rcc` | red blood cell count |
| `wcc` | white blood cell count |
| `hc` | hematocrit, percent |
| `hg` | hemaglobin concentration |
| `ferr` | plasma ferritins |
| `ht` | height, cm |
| `wt` | weight, kg|
| `sex` | either `f` or `m` |
| `sport` | Takes on the following values: `B_Ball`, `Field`, `Gym`, `Netball`, `Row`, `Swim`, `T_400m`, `T_Sprnt`, `Tennis`, `W_Polo`|

### Exercises
1. **(CW) Read the following csv into a data frame called `ais` in R: https://drive.google.com/file/d/1WY7MHz3TnBvMPYJXq8UecPrhgAt8krAJ/view?usp=sharing**
1. **(CW) Find the pair-wise correlation for all quantitative variables using `cor()` (you will need to use `select()` to remove `sex` and `sport`).**
1. **(CW) Plot the pair-wise scatterplots for all quantitative variables using `pairs()` (you will need to use `select()` to remove `sex` and `sport`).**
1. **(CW) Based on the correlation matrix, which two variables have the **highest** correlation? Use `cor.test()` to find more details about the correlation of these two variables (what is the p value? What is the confidence interval?)**
1. Based on the correlation matrix, which two variables have the **lowest** correlation? Use `cor.test()` to find more details about the correlation of these two variables (what is the p value? What is the confidence interval?)
1. Find the pair of variables with the lowest correlation and a p value of < 0.05.
1. Try filtering by sex or sport and check how the pairwise correlations change. Do the variables have higher or lower correlations after filtering?

## Part 3: Regression

### Code from class:
```
# perform a linear regression with temperature_F as the independent variable and count as the dependent variable
bike_regression <- lm(count ~ temperature_F, data = bike_sharing)

# summarize the regression output
summary(bike_regression)
```

### Exercises
1. Of height and weight, which do you presume is the independent variable?
2. **(CW) Perform a linear regression on height and weight. What is the slope of the regression line? What is the p value?**
3. How do these values change when you reverse the order of the variables?
4. Try performing linear regressions for the pairs of variables you found correlations for in the previous section.
5. Plot two quantitative variables against each other. If you use `geom_smooth(method=lm)`, the linear regression line will be plotted. Try this out.

