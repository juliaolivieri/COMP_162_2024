# Classwork 7: Data Visualization with ggplot2


## Part 1: Making your first plot

### Code from class

```
# install the tidyverse package if you haven't already
install.packages("tidyverse")

# load in the tidyverse package
library(tidyverse)

# make a scatterplot of displ vs hwy
ggplot(data = mpg) +
  geom_point(mapping = aes(x = displ, y = hwy))

ggsave("my_first_plot.png")
```

### Exercises
1. **(CW) Open a new R script file. This is what you will turn in for today's classwork.**
1. **(CW) If you haven't already, install the "tidyverse" library using `install.packages("tidyverse")**
1. **(CW) Load the "tidyverse" library.**
1. View the dataset mpg with `View(mpg)` (this dataset is pre-loaded with the tidyverse package).
1. **(Classwork) Use the code above to create a plot of `displ` vs `hwy`.**
1. **(Classwork) Save this plot using `ggsave()` (example command above). You may want to set your working directory to a convenient place for the plot to be output.**
1. **(Classwork) Make a scatterplot of `hwy` versus `cyl`.**
1. What can you conclude from this scatterplot?
1. Run `ggplot(data = mpg)`. What do you see?
1. Try switching `hwy` and `displ` between the two axes. 
1. Try using the following commands from last lecture on this data: `head(mpg)`, `head()`, `summary()`, `str()`. 
1. How many rows does `mpg` have? How many columns?
1. What does the `drv` variable describe? Read the help for `?mpg` to find out.
1. What happens if you make a scatterplot of `class` versus `drv`? Why is the plot not useful?
 
## Part 2: Changing plot aesthetics

### Code from class
```
# color points in the scatterplot by class
ggplot(mpg) +
  geom_point(aes(displ, hwy, color = class)) 

# using multiple aesthetics
ggplot(mpg) +
  geom_point(aes(displ, 
                 hwy, 
                 color = class, 
                 shape = drv, 
                 size = cyl,
                 alpha = year))

```

### Exercises
1. **(CW)Plot `cty` vs `hwy` and color by `drv`, determine shape by `fl`, and size by `displ`.**
1. Make three different plots of `cty` vs `hwy`, the first colored by `drv`, the second with shape determined by `fl`, and the third with size determined by `displ`.
1. Is it easier to see patterns in the plot from 1. or the plot from 2.?
1. Plot `displ` vs `cty`. Try mapping color to `hwy`. What happens?
1. Try mapping a quantitative variable to shape. What happens?
1. Try mapping a categorical variable to size. What happens?
1. What happens if you map the same variable to multiple aesthetics?
1. What happens if you map an aesthetic to something other than a variable name, like `aes(color = displ < 5)`
