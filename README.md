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
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: SANJAI.R
RegisterNumber:  212223040180
*/
```
```py
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
X_mean=np.mean(X)
print(X_mean)
Y_mean=np.mean(Y)
print(Y_mean)
num=0
denum=0
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2
m=num/denum
print(m)
b=Y_mean - m*X_mean
print(b)
Y_pred=m*X+b
print(Y_pred)
plt.scatter(X,Y,color='blue')
plt.plot(X,Y_pred,color='yellow') 
plt.show()

```
## Output:
# input values are
![Screenshot 2024-09-30 085551](https://github.com/user-attachments/assets/8dea49a0-e663-4fc8-ab43-4fdbeea2a799)
# slope:
![Screenshot 2024-09-30 085609](https://github.com/user-attachments/assets/03d0351c-f044-4c74-8ac3-82b1a80121cc)
# y_intercept:
![Screenshot 2024-09-30 085630](https://github.com/user-attachments/assets/65c95efc-9c76-4cf4-8092-0a4c8a595b05)


# y_predict:
![Screenshot 2024-09-30 085701](https://github.com/user-attachments/assets/b9f38855-3f4d-48fc-9a7f-d3fac6508436)




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
