# Classwork 6

## Mathematical Operators in R

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

## Mathematical functions in R

| Function | Description |
| -- | -- |
| `abs(x)` | Absolute value of x |
| `sqrt(x)` | Square root of x |
| `log(x)` | Natural log of x |
| `log10(x)` | Log base 10 of x |
| `floor(x)` | x rounded down |
| `ceiling(x) | x rounded up |

1.
  * Open a new R script.
  * Assign a variable `var1` to the result of five different mathematical operations (e.g. `(5*10 %/% -3)^2 + 10/0.5`)
  * Assign a variable `var2` to the result of a combination of mathematical operations and functions (e.g. `abs(89 %% 5) + sqrt(log(95))`)
  * Assign a third variable `var3` to `var1 > var2`.
  * Print each variable. Is `var1 > var2`?
  * Check the type of each variable using the `str()` function (e.g. `str(var1)`)
  * Which variable types are missing? Try assign variables to these types, and check with the `str()` function
  * **(Challenge - not required)** Define variables `X1`, `X2`, `t`, `s1`, `s2`, `n1`, `n2`. Set them equal to quantitative values of your own choosing. Then write an expression in terms of those variables to calculate $$(X_1 - X_2) + t\sqrt{\frac{s_{1}^2}{n_1} + \frac{s_2^2}{n_2}}$$
