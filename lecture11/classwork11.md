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
