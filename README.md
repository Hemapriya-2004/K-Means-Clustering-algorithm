# Implementation of K-Means Clustering Algorithm
## Aim
To write a python program to implement K-Means Clustering Algorithm.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation

## Algorithm:

### Step1
loadthe csv into a dataframe

### Step2
print the number of contents to be display using df.head().

### Step3
the number of rows returned is defined in pandas option settings

### Step4
check your system's maximum column with the pd.options.display.max_column statement

### Step5
increase the maximum number of rows to display the entire dataframe

## Program:
```

import pandas as pd
from sklearn import linear_model
import matplotlib.pyplot as plt

df = pd.read_csv("cars.csv")

X = df[['Weight', 'Volume']]
y = df['CO2']

regr = linear_model.LinearRegression()
regr.fit(X,y)
#Cofficients and intercept of Model
print('Coefficients: ', regr.coef_) 
print('Intercept: ',regr.intercept_)

#predict the CO2 emission of a car where the weight is 300kg, and the volume is 1300cm3:
predictedCO2 = regr.predict([[3300, 1300]])
print('Predicted CO2 for the corresponding weight and volume', predictedCO2)

```
## Output:

![output](https://github.com/Hemapriya-2004/K-Means-Clustering-algorithm/blob/master/k1.jpg?raw=true)

![output](https://github.com/Hemapriya-2004/K-Means-Clustering-algorithm/blob/master/k2.jpg?raw=true)

## Result
Thus the K-means clustering algorithm is implemented and predicted the cluster class using python program.
