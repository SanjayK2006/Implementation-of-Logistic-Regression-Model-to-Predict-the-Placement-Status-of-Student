# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: 
RegisterNumber:
```
```
import pandas as pd
data=pd.read_csv("C:/Users/admin/Downloads/placement 21212.csv")
data.head()
```
```
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
data.head()
```
```
data1.isnull()
```
```
data1.duplicated().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"])
data1["status"]=le.fit_transform(data1["status"])
data1
```
```
x=data1.iloc[:,:-1]
x
```
```
y=data1["status"]
y
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
```
```
from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
y_pred
```
```
from sklearn.metrics import accuracy_score
accuracy_score(y_test,y_pred)
```
```
from sklearn.metrics import classification_report
classification_report1=classification_report(y_test,y_pred)
print(classification_report1)
```
```
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])
```
```

*/
```

## Output:
![Screenshot (11)](https://github.com/SanjayK2006/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144979178/7b0040dc-1386-4b1e-98db-65cee3789f23)
![Screenshot (12)](https://github.com/SanjayK2006/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144979178/8cbeb3c1-a393-4923-a1cf-d40a9584902f)
![Screenshot (13)](https://github.com/SanjayK2006/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144979178/a43a1e07-b64e-4011-992e-764cdf862b8a)
![Screenshot (14)](https://github.com/SanjayK2006/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144979178/193abd6b-ef12-492f-bab1-b0363c2ad760)
![Screenshot (15)](https://github.com/SanjayK2006/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144979178/ff7d9deb-26c2-4bee-af10-3e58526c18ab)
![Screenshot (16)](https://github.com/SanjayK2006/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/144979178/04240e1b-f7e6-45ab-b2f4-797346d7994f)



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
