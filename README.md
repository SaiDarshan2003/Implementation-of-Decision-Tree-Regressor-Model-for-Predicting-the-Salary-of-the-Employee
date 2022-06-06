# Implementation of Decision Tree Regressor Model for Predicting the Salary of the Employee
## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm
1. 
2. 
3. 
4. 
## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Sai Darshan G
RegisterNumber:  212221240047
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
x=data[["Position","Level"]]
y=data["Salary"]
from sklearn.model_selection import train_test_split
X_train,X_test,Y_train,Y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(X_train,Y_train)
y_pred=dt.predict(X_test)
from sklearn import metrics
mse=metrics.mean_squared_error(Y_test,y_pred) 
r2=metrics.r2_score(Y_test,y_pred)
mse
r2
dt.predict([[5,6]])
```
## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](2.png)
## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
