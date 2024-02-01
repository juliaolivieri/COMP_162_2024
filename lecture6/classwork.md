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

## Variable assignment
  * **(CW) Create a new R script file, and save it as classwork6.R. You will submit this file for the "classwork 6" assignment.**
  * **(CW) Assign a variable `var1` to an integer value.**
  * **(CW) Assign a variable `var2` to the result of a combination of mathematical operations and functions (e.g. `abs(89 %% 5) + sqrt(log(95))`)**
  * Assign a third variable `var3` to `var1 > var2`.
  * **(CW) Print each variable**
  * Is `var1 > var2`?
  * **(CW) Check the type of each variable using the `str()` function (e.g. `str(var1)`)**
  * Which variable types are missing? Try assign variables to these types, and check with the `str()` function
  * Define variables `X1`, `X2`, `t`, `s1`, `s2`, `n1`, `n2`. Set them equal to quantitative values of your own choosing. 
  * Write an expression in terms of those variables to calculate $$(X_1 - X_2) + t\sqrt{\frac{s_{1}^2}{n_1} + \frac{s_2^2}{n_2}}$$
  
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
