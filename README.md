# developed by : shakthivel v
# register no : 24901278


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
    import numpy as np 
    import matplotlib.pyplot as plt
    x = np.array([0,1,2,3,4,5,6,7,8,9])
    y = np.array([1,3,2,5,7,8,8,9,10,12])
    plt.scatter(x,y)
    plt.show()
    xmean = np.mean(x)
    ymean = np.mean(y)
    num=0
    den=0
    for i in range(len(x)):
        num+=(x[i]-xmean)*(y[i]-ymean)
        den+=(x[i]-xmean)**2
    m = num/den
    b = ymean - m*xmean
    print(m,b)
    ypred = m*x+b
    print(ypred)


    plt.scatter(x,y,color='Red')
    plt.plot(x,ypred,color='Blue')
    plt.show()





```
## Output
![Screenshot 2024-12-30 144014](https://github.com/user-attachments/assets/3df29d3b-825e-455d-b4bd-b50a9e295048)
![Screenshot 2024-12-30 144045](https://github.com/user-attachments/assets/390a99d0-6e3b-4187-ad70-7bdfc780db29)
![Screenshot 2024-12-30 144056](https://github.com/user-attachments/assets/6182c414-4259-416a-9bf5-0e4109cf22e8)
![Screenshot 2024-12-30 144105](https://github.com/user-attachments/assets/6a0e6a99-1277-410b-9b6a-19f98732d2a8)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
