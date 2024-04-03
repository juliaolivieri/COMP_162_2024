## Part 1: Linear regression with multiple independent variables

### Code from class

```
X_train, X_test, y_train, y_test = model_selection.train_test_split(aq[["CO", "NMHC", "NOx"]], aq[[“O3”]], test_size = 0.2, random_state=123)

reg = linear_model.LinearRegression().fit(X_train, y_train)

reg.score(X_test, y_test)

pd.DataFrame({"column" : X_test.columns, "coefficient" : reg.coef_}).sort_values("coefficient")
```

### Exercises

1. Try training a linear regression model on all of the quantitative variables from the SAT scores dataset (remember to split into train and test set).
1. Find the score of this model. How does it compare to the score of models trained on a single variable?
1. Find the coefficients corresponding to each column. Which column has the largest-magnitude coefficient? Smallest-magnitude? Does this breakdown make sense to you?
1. What happens if you include the dependent variable in the training set?
1. Try training a model with only a subset of the independent variables. How does the model perform?
1. Download the apple quality dataset: https://drive.google.com/file/d/1MJGf7XJSdrGCy6hKDtvS9rt5HvlevMK6/view?usp=sharing. Decide on a column to use as the dependent variable. Try predicting the dependent variable based on the independent variables. Which independent variables are most useful for predicting the dependent variable?


Fill out quiz preference: https://forms.gle/fSPNLgvUtWSrg9L78 
