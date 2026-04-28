# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula.
 <img width="462" height="199" alt="WhatsApp Image 2026-04-24 at 4 12 58 PM" src="https://github.com/user-attachments/assets/255a2726-0940-4c12-8b82-a76d90ccb756" />

4 Compute the y -intercept of the line by using the formula:
     
      b=Yˉ−mXˉ
5. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation
Y=mX+b and plot the scatterplot

## Program:
```python
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: 
RegisterNumber:
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score

df = pd.read_csv("student_scores.csv.xls")
df.head(10)

plt.scatter(df['Hours'], df['Scores'])
plt.xlabel('Hours')
plt.ylabel('Scores')
x = df.iloc[:,0:1]
y = df.iloc[:,-1]

from sklearn.model_selection import train_test_split
X_train, X_test, Y_train, Y_test = train_test_split(x,y,test_size=0.2, random_state=0)

from sklearn.linear_model import LinearRegression
lr = LinearRegression()
lr.fit(X_train, Y_train)

y_pred = lr.predict(X_test)

plt.scatter(df['Hours'],df['Scores'])
plt.xlabel('Hours')
plt.ylabel('Scores')
plt.plot(X_train, lr.predict(X_train), color='red')

lr.coef_
lr.intercept_

mse = mean_squared_error(Y_test, y_pred)
rmse = np.sqrt(mse)
mae = mean_absolute_error(Y_test, y_pred)
r2 = r2_score(Y_test, y_pred)

print("MSE:", mse)
print("RMSE:", rmse)
print("MAE:", mae)
print("R2:", r2)
*/

```

## Output:
<img width="826" height="640" alt="image" src="https://github.com/user-attachments/assets/582bdf35-922b-403c-8f3b-c1b4941813f4" />





## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
