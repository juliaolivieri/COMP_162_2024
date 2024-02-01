# Classwork 6

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

1.
  * Open a new R script for today's classwork.
  * Assign a variable `var1` to the result of five different mathematical operations (e.g. `(5*10 %/% -3)^2 + 10/0.5`)
  * Assign a variable `var2` to the result of a combination of mathematical operations and functions (e.g. `abs(89 %% 5) + sqrt(log(95))`)
  * Assign a third variable `var3` to `var1 > var2`.
  * Print each variable. Is `var1 > var2`?
  * Check the type of each variable using the `str()` function (e.g. `str(var1)`)
  * Which variable types are missing? Try assign variables to these types, and check with the `str()` function
  * **(Extra - not required)** Define variables `X1`, `X2`, `t`, `s1`, `s2`, `n1`, `n2`. Set them equal to quantitative values of your own choosing. Then write an expression in terms of those variables to calculate $$(X_1 - X_2) + t\sqrt{\frac{s_{1}^2}{n_1} + \frac{s_2^2}{n_2}}$$
  
2.
* Try creating a vector by combining a numeric, logical, and character element.
* Use the `str()` function to check the type of the resulting vector.
* Copy the following vectors into your script: 
```
tesla_price <- c(131.49, 128.78, 127.17, 133.42, 143.75, 143.89, 144.43, 160.27, 177.9)
apple_price <- c(135.94, 135.21, 135.27, 137.87, 141.11, 142.53, 141.86, 143.96, 145.93)
```
* Use the `length()` command to check the length of each vector.
* Add these two vectors.
* Compare these two vectors using `>`.
* Subtract one vector from the other.
* Combine the two vectors using `c()`. Find the length of the result.
* **(Extra - not required)**
 * Find the sum of the first four entries of the `tesla_price` vector.
 * Subset both vectors to only the first, third, and 6th entries, and then subtract these two sub-vectors.

