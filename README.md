# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
### Program to implement univariate Linear Regression to fit a straight line using least squares.

```
Developed by: Keerthika N
RegisterNumber: 212221230049
```

```
import numpy as np
import matplotlib.pyplot as plt

# Preprocessing Input data
x=np.array(eval(input("Enter array X: ")))
y=np.array(eval(input("Enter array Y: ")))

# Mean
x_mean=np.mean(x)
y_mean=np.mean(y)

# For slope
num,denom=0,0  

# To find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(x)):
  num+=((x[i]-x_mean)*(y[i]-y_mean))
  denom+=(x[i]-x_mean)**2

# Calculate slope
m=num/denom
print("Slope: ",m)

# Calculate intercept
b=y_mean-m*x_mean
print("Intercept: ",b)

# Line equation
y_predicted=m*x+b
print(y_predicted)

# To plot graph
plt.scatter(x,y,color='pink')
plt.plot(x,y_predicted,color='blue')
plt.show()

# Predict y if x=3
y_3=m*3+b
print("If x=3 then y=",y_3)

# Sample input:
# 8,2,11,6,5,4,12,9,6,1
# 3,10,3,6,8,12,1,4,9,14
```

## Output:


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
