# Classwork 6

Note: "classwork" questions are bolded. You are welcome to include more answers in your classwork submission.

### Mathematical Operators in R

| Operator | Description |
| -- | -- |
| `+` | Addition |
| `-` | Subtraction|
|`*` | Multiplication |
| `/` | Division |
| `^` | Exponent |
| `%%` | Modulo |
| `%/%` | Floor division |
| `>` | Greater than | 
| `<` | Less than | 
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |
| `!=` | Not equal to | 
| `==` | Equal to |

### Mathematical functions in R

| Function | Description |
| -- | -- |
| `abs(x)` | Absolute value of x |
| `sqrt(x)` | Square root of x |
| `log(x)` | Natural log of x |
| `log10(x)` | Log base 10 of x |
| `floor(x)` | x rounded down |
| `ceiling(x)` | x rounded up |

### Variable types in R

| Variable type | Abbreviation | Example |
| -- | -- | -- |
| Character | chr | 'R', 'Hello world'|
|Numeric | num | 6.2, 4.13, -3 |
|Integer | int | 3L, -1L, 12L |
| Logical | logi | TRUE, FALSE, T, F |

### Example code from lecture

```
# Assigning variables
my_variable <- 100
my_variable = 100
print(my_variable)

# Using mathematical operations and functions
x <- ((5*2) + abs(3 - 10)) %% 2
str(x)

# vectors
is.vector(5)
is.vector("hello")
c(5,10)
days <- c("Monday", "Tuesday", "Wednesday", "Thursday", "Friday")
length(days)
str(days)

# Indexing
nums <- c(3,5,2,30)
nums[1]
nums[1:3]
nums[2:length(nums)]
nums[c(2,4)]

# Mathematical operations on vectors
x <- c(4, 5, 2, -1)
y <- c(-2, 4, 9, 0)
x + y
```

## Exploring R Studio
1. **(CW) Create a new R script file, and save it as classwork6.R. You will submit this file for the "classwork 6" assignment.**
1. **(CW) Add a comment to the beginning of your script by using #. What happens when you try to run this line of code? I recommend including comments throughout this classwork to 1. help you remember what you did.**
1. Evaluate the mathematical expression (400/20) + 22 in the console. Then add it to your script file, and evaluate it there. Is there a difference? Which is preferrable?
1. Try writing -3:6 in your script and evaluating it. What is the output? What do you think the output will be if you instead input 4:93? Check to see if you were right.
1. Check the documentation of the min function by running ?min in your script. What does this function do based on the documentation?
1. At the bottom of the documentation you should see some lines of code starting with require(stats); require(graphics) and ending with  identical(n0, pmax(n0, 4))). Copy these lines of code into your script, highlight them, and press "Run." Do you see a plot appear in the "Plots" pane?
1. After running this code, some objects should appear in the "Environment" RStudio pane. This is where you will see all the objects you have defined in your session.

## Mathematical Operations in R
1. **(CW) One of the most basic uses of R is as a calculator. Write down a line of code in your script to calculate the number of seconds in a year. Include a comment above it to keep track of what you were trying to calculate.**
1. Use the %% operator to check whether the following number is even: (3.2^2) %/% 2
1. Use > to check whether sqrt(3) is greater than log(3).
1. Use < to check whether log(3) is less than log10(3).
1. R has the value of pi encoded in this variable: Try executing pi in your R script.
1. (Challenge) A penny has a diameter of 0.750 mm. A quarter has a diameter of 24.26 mm. Calculate the difference in the areas of a quarter and a penny. Remember, the area of a circle is equal to $$\pi (radius)^2$$, and $$radius = diameter/2$$.

## Assigning/printing variables
1. **(CW) Assign a variable to var1 with the result of 5 different mathematical operations/functions, e.g. floor((27 - 3) %% 5) + ceiling(-5.9)^2.**
1. Assign a variable var2 to a different result of mathematical operations/functions.
1. Assign a third variable to the result of var1 == var2.
1. Assign var4 to T.
1. Assign var5 to TRUE.
1. Check whether var4 is equal to var5 using ==.
1. Print each variable.
1. (Challenge) Redo question 7 from the section "Mathematical Operations in R", but this time assign a variable for the diameter of a quarter, a variable for the diameter of a penny, a variable for the area of a quarter, a variable for the area of a penny, and a variable for the difference in area of the two.
  
## Vectors
* Create a vector by combining a numeric, logical, and character element (e.g. `c(5, TRUE, "tiger")`)
* Use the `str()` function to check the type of the resulting vector.
* **(CW) Copy the following vectors into your script:** 
```
tesla_price <- c(131.49, 128.78, 127.17, 133.42, 143.75, 143.89, 144.43, 160.27, 177.9)
apple_price <- c(135.94, 135.21, 135.27, 137.87, 141.11, 142.53, 141.86, 143.96, 145.93)
```
* **(CW) Use the `length()` command to check the length of each vector.**
* Add these two vectors.
* Compare these two vectors using `>`.
* **(CW) Subtract one vector from the other.**
* Combine the two vectors using `c()`. Find the length of the result.
* Find the sum of the first four entries of the `tesla_price` vector.
* Subset both vectors to only the first, third, and 6th entries, and then subtract these two sub-vectors.

## Working with dataframes
* Use the `data()` function to explore the datasets available in R and load one.
* Try the following commands on your dataset. What does each one tell you about the data that wasn't evident from the previous functions?
```
head()
View()
str()
summary()
```
* Try the command `table()` on one of the categorical columns of the dataset. What does it tell you?
* Subset the dataframe to just the 3rd through 20th row, and the second and fourth columns.
* Try adding or multiplying two of the columns and saving the values in a new column
