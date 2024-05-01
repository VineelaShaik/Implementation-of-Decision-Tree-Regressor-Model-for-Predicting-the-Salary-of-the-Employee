# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
step 1.Start

step 2.Import pandas

step 3.Import Decision tree classifier

step 4.Fit the data in the model

step 5.Find the accuracy score

step 6.Stop
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Vineela Shaik
RegisterNumber:212223040243
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
x.head()

y=data[["Salary"]]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])

*/
```

## Output:
#### data.head()
![Screenshot 2024-04-29 143854](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145917810/305d2c04-01f2-465e-8953-4acde0713fbf)

#### data.info()
![Screenshot 2024-04-29 143901](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145917810/df271736-47a0-447b-ba19-beda38d16a77)

#### isnull() and sum()
![Screenshot 2024-04-29 143910](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145917810/33581fd8-b8df-4ce0-b377-d2559b1b8e4e)

#### data.head() for salary 
![Screenshot 2024-04-29 143917](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145917810/190a42cc-6c91-4b5e-b48d-3f7be30871fc)

#### MSE value
![Screenshot 2024-04-29 143724](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145917810/939edbfa-455b-4470-990e-010f7618bb4f)

#### r2 value
![Screenshot 2024-04-29 143733](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145917810/a994dac2-840f-4b76-a6eb-9ab12ab8a31e)

#### data prediction
![Screenshot 2024-04-29 143740](https://github.com/Aadithya2201/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145917810/c73ce68c-a5c1-4c3f-80c0-5970c8115ddf)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
