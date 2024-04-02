# Classwork 18

## Part 1: Correlation

### Code from Class

```
aq.corr()

aq.corr(method = "pearson")
aq.corr(method = "spearman")

sns.heatmap(aq.corr(),annot=True)
plt.show()
```

### Exercises

1. **(CW) Load the SAT scores dataset into your notebook. Data available here: [https://drive.google.com/file/d/1zxa8ekinJdsucWvtrVmpxazYM8oSo0DA/view?usp=sharing](https://drive.google.com/file/d/10dzC5BrHOmgrtzJ6PWPgGH08cg-vg4B7/view?usp=sharing)**
1. **(CW) Calculate the Spearman and Pearson correlation matrices.**
1. **(CW) Which pair of variables have the largest-magnitude positive correlation?**
1. **(CW) Which pair of variables have the largest-magnitude negative correlation?**
1. Plot the Spearman and Pearson correlation matrices.

## Part 2: Introduction to Machine Learning

### Exercises

1. What is your current understanding of the term “machine learning”?
1. If a machine learning task involves predicting the percentage of a student's score in an exam, which type of task is it?
   * Regression
   * Classification
1. If a machine learning task involves predicting whether a customer will make a purchase or not, which type of task is it?
   * Regression
   * Classification
1. If a machine learning task involves predicting a person's age based on their social media usage, given a dataset with ages and corresponding social media usage data, which type of learning is it?
   * Supervised learning
   * Unsupervised learning
1. If a machine learning task involves grouping similar news articles together without prior knowledge of their categories, which type of learning is it?
   * Supervised learning
   * Unsupervised learning
  
## Part 3: Linear Regression

### Code from class

```
from sklearn import linear_model
from sklearn import model_selection
from sklearn import metrics

reg = linear_model.LinearRegression().fit(salaries[["YearsExperience"]],salaries[["Salary"]])

print(reg.coef_)
print(reg.intercept_)

X_train, X_test, y_train, y_test = model_selection.train_test_split(salaries[["YearsExperience"]], salaries[["Salary"]], test_size = 0.2, random_state=1234)
   
reg = LinearRegression().fit(X_train, y_train)
y_pred = reg.predict(X_test)
   
metrics.r2_score(y_test, y_pred)
metrics.mean_squared_error(y_test, y_pred)
```

### Exercises
1. Import all necessary sklearn modules:
   ```
   from sklearn import linear_model
   from sklearn import model_selection
   from sklearn import metrics
   ```
1. For the "scores" dataset, "Average Score (SAT Writing)" will be the dependent variable. Choose a column to use as the predictor variable (independent variable).
1. Split the data into a training and testing set.
1. Train a new linear model using the training data.
1. “Predict” the independent variable from the training set using this model. Use `metrics.r2_score()` and  `metrics.mean_squared_error()` to evaluate the prediction.
1. “Predict” the independent variable from the testing set using this model. Use `metrics.r2_score()` and  `metrics.mean_squared_error()` to evaluate the prediction.
1. Which prediction is the most accurate? Least? Does this make sense to you?
1. Try a few different random seeds for the train/test split. How different are your answers?
1. Which variable provides the most accurate predictions?
