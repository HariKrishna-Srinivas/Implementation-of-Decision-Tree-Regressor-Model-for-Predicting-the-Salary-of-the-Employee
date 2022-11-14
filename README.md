# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
STEP 1:
Import the required libraries.

STEP 2:
Upload the csv file and read the dataset.

STEP 3:
Check for any null values using the isnull() function.

STEP 4:
From sklearn.tree inport DecisionTreeRegressor.

STEP 5:
Import metrics and calculate the Mean squared error.

STEP 6:
Apply metrics to the dataset, and predict the output.
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: M.Harikrishna
RegisterNumber: 212221230059


import pandas as pd
data = pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()
x = data[["Position","Level"]]
y = data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)
from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse
r2 = metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

*/
```

## Output:

DATA HEAD:

![image](https://user-images.githubusercontent.com/94882905/201613209-8a84be5a-137e-41e7-99e8-d28a9909e2ed.png)

DATA INFO:

![image](https://user-images.githubusercontent.com/94882905/201613331-cce214bc-237d-4b31-ad6a-6635ac59628f.png)

DATA ISNULL:

![image](https://user-images.githubusercontent.com/94882905/201613416-debd911c-5575-4590-85f6-e524c3818590.png)

DATA HEAD:

![image](https://user-images.githubusercontent.com/94882905/201613511-52dd3e90-b506-4887-8b44-c91883e1265a.png)

dt.FIT:

![image](https://user-images.githubusercontent.com/94882905/201613620-64f5d3a7-b445-4b2d-b470-330719ccb955.png)

MSE:

![image](https://user-images.githubusercontent.com/94882905/201613724-c2360c2a-e945-4624-a8b7-4a9fc3276f36.png)

R2:

![image](https://user-images.githubusercontent.com/94882905/201613834-9c6eca09-16cd-492d-bd8e-4579630fe071.png)

PREDICT VALUE:

![image](https://user-images.githubusercontent.com/94882905/201614040-c2b8a50d-f61b-4d51-9efe-badb1d765d1a.png)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
