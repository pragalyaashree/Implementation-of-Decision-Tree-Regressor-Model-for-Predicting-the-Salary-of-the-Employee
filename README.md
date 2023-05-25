# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas to read the csv files.
2. Display the head and tail of the dataset.
3. Import LabelEncoder() from sklearn.preprocessing.
4. Label the data which are not in the integer type.
5. Assign the X and Y from the dataset.
6. Split the dataset using train_test_split from sklearn.model_selection.
7. nImport DecisionTreeRegressor from sklearn.tree
8. Fit the Training set in a variable.
9. Import metrics from sklearn to find the Mean Squared Error.
10. Predict the result for the given values.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: R.K Pragalyaa shree
RegisterNumber: 212221040125
*/
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
x = data[["Position","Level"]]
x.head()
y = data["Salary"]
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```
## Output:
### 1. data.head()
![image](https://github.com/balaji-21005757/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94372294/58d334dd-2313-4af4-8547-92eed75bcfb5)
### 2. data.info()
![image](https://github.com/balaji-21005757/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94372294/b5dcb774-d410-46eb-9866-2e8626bfaddf)
### 3. isnull() and sum()
![image](https://github.com/balaji-21005757/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94372294/ce234c06-6da2-4559-8e81-cd2f67a70666)
### 4. data.head() for salary 
![image](https://github.com/balaji-21005757/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94372294/11d76c7f-eedd-4660-9994-7642a1a5e1e9)
### 5. MSE value
![image](https://github.com/balaji-21005757/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94372294/65f1a917-84d9-4eea-b103-5abff8aa1d3a)
### 6. r2 value
![image](https://github.com/balaji-21005757/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94372294/0c36d354-e42d-4ba1-82d1-f4dfd6466de2)
### 7. data prediction
![image](https://github.com/balaji-21005757/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94372294/d8458904-8abe-445d-a4ad-9493174ab1ac)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
