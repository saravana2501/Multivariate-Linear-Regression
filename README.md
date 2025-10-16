# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
Step1:
Import Libraries Import the required libraries: pandas for data handling and linear_model from sklearn for linear regression.

Step2:
Load Dataset Read the CSV file (carsemission.csv) using pandas and store it in a DataFrame.

Step3:
Prepare Data Select the features Weight and Volume as input (X), and CO2 as the target/output (y).

Step4:
Train the Model Create a Linear Regression model and train (fit) it using the input (X) and output (y) data.

Step5:
Display Model Parameters Print the learned coefficients (slopes for Weight and Volume) and the intercept (bias term).

Step6:
Make Predictions Predict the CO2 emission for a new car with given Weight and Volume, and print the result.

## Program:
```

import pandas as pd
from sklearn import linear_model
df = pd.read_csv("/content/carsemission.csv")
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

### Insert your output

<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
