# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import the required libraries such as NumPy, Pandas and Scikit-learn.

### Step2
Load the dataset and separate input and output variables.

### Step3
Split the dataset into training and testing data.

### Step4
Train the Multivariate Linear Regression model using training data.

### Step5
Predict the output using the trained model and display the results.

## Program:
```
Developed by: Logapriya A
Register number:212225040202
# Dataset Setup - Run this cell before starting the experiment

import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")

import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)





```
## Output:

![Uploading Screenshot 2026-11-20 221527.png…]()


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
