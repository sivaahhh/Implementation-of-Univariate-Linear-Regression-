# Implementation-of-Univariate-Linear-Regression-

AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

Equipments Required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Jupyter notebook
Algorithm
Get the independent variable X and dependent variable Y.
Calculate the mean of the X -values and the mean of the Y -values.
Find the slope m of the line of best fit using the formula.
image

4. Compute the y -intercept of the line by using the formula:
image

5. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the scatterplot.
Program:

Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: SIVA SAKTHI A
RegisterNumber:  212224223005
```
import numpy as np
import matplotlib.pyplot as plt

# 1. Input data
x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])

# 2. Compute the means
x_mean = np.mean(x)
y_mean = np.mean(y)

# 3. Calculate numerator and denominator
num = 0
denom = 0

for i in range(len(x)):
    num += (x[i] - x_mean) * (y[i] - y_mean)
    denom += (x[i] - x_mean) ** 2

# 4. Compute slope and intercept
m = num / denom
b = y_mean - m * x_mean

# 5. Predict y values
y_predicted = m * x + b
print("Predicted values:", y_predicted)

# 6. Display results
print("Slope:", m)
print("Intercept:", b)
print("Regression equation: y =", m, "x +", b)

# 7. Plot the results
plt.scatter(x, y, label="Actual data")
plt.plot(x, y_predicted, color="red", label="Regression line")
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Univariate Linear Regression")
plt.legend()
plt.grid(True)
plt.show()
```

Output:
<img width="997" height="650" alt="image" src="https://github.com/user-attachments/assets/dc3405b5-1836-47cf-a5a2-21cf1054253e" />

Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
