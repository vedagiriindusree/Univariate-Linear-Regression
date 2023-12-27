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
'''
#Developed by: Vedagiri Indu sree
#Register Number: 23004520
'''
import numpy as np
import matplotlib.pyplot as plt
X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])
XMean=np.mean(X)
YMean=np.mean(Y)
num,den=0,0
for i in range(len(X)):
  num+=(X[i]-XMean)*(Y[i]-YMean)
  den+=(X[i]-XMean)**2
m=num/den
c=YMean-m*XMean
print(m,c)
Y_Pred=m*X+c
print(Y_Pred)
plt.scatter(X,Y)
plt.plot(X,Y_Pred,color="red")
plt.show()
```
## Output
![image](https://github.com/vedagiriindusree/Univariate-Linear-Regression/assets/149366776/d1a2506b-4c6d-4199-a638-6784d42138df)

![image](https://github.com/vedagiriindusree/Univariate-Linear-Regression/assets/149366776/ab40701d-fcf5-4906-b128-d887d54c45a8)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
