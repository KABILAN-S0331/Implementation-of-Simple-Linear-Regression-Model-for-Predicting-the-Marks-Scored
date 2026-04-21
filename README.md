# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm :

### 1. Import the required libraries and initialize the dataset for hours studied (X) and marks scored (Y).
### 2. Create and train the simple linear regression model using the given data.
### 3. Obtain the slope (m) and intercept (b), and use the model to predict marks for a given input.
### 4. Plot the actual data points and the regression line to visualize the relationship.

## Program:
### Program to implement the simple linear regression model for predicting the marks scored.
### Developed by: Kabilan S
### RegisterNumber: 212225230119
```
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([30, 45, 55, 85, 99])
model = LinearRegression()
model.fit(X, Y)
m = model.coef_[0]
b = model.intercept_
print("Slope (m):", m)
print("Intercept (b):", b)
x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])

Y_pred = model.predict(X)
plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()

```

## Output:
<img width="1033" height="520" alt="image" src="https://github.com/user-attachments/assets/fb2dfcd5-1f9a-4a52-8c7c-431e812acb7f" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
