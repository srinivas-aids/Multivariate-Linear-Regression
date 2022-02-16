# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import Pandas library and linear_model from sklearn using import statement.



### Step2
Read the given csv file using read_csv() method

### Step3
Create two arrays, independent array x with two classes and dependent array y with one class. Find the regression of x and y using linear_model.LinearRegression() method and fit x and y usind .fit() method.

### Step4
Find the coefficients using .coef_ and intercept using .intercept_ .

### Step5
Predict the liner regression using regr.predict() method and display the result.

## Program:
```
import pandas as pd
from sklearn import linear_model
import matplotlib.pyplot as plt

df=pd.read_csv("cars.csv")

x=df[['Weight', 'Volume']]
y=df['CO2']

regr=linear_model.LinearRegression()
regr.fit(x,y)

#coefficients and intercept of model
print('Coefficients:', regr.coef_)
print('Intercept:',regr.intercept_)

#predict the CO2 emission of a car when the weight is 3000 kg, and the volume is 1300cm3

predictedCO2= regr.predict([[3300, 1300]])
print('Predicted CO2 for the corresponding weight and volume',predictedCO2)
```
## Output:
![output](./images/111.jpg)

### Insert your output

<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.