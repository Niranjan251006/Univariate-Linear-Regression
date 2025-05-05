# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
Developed by: your name: NIRANJAN S
RegisterNumber: 212224040221
```
```
import numpy as np
import matplotlib.pyplot as plt

X = np.array(eval(input()))
Y = np.array(eval(input()))

Xmean = np.mean(X)
Ymean = np.mean(Y)
num,den = 0,0
for i in range(len(X)):
    num += (X[i]-Xmean)*(Y[i]-Ymean)
    den += (X[i]-Xmean)**2
m = num/den
c = Ymean-m*Xmean
    
print (m, c)

Y_pred = m*X + c
print (Y_pred)

plt.scatter(X,Y)
plt.plot(X,Y_pred,color="red")
plt.show()

```
## Output
![293221163-e29c9cee-a863-4eaa-8a54-36dd64f66b6e](https://github.com/user-attachments/assets/1b05cd8b-d80c-4ae1-ae6a-2688c2ee796e)
![293221288-1025d99f-f4bb-462c-b791-478bfa7579c0](https://github.com/user-attachments/assets/b11baf91-7b0f-4043-91af-83d0e9211d46)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
