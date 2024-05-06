# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
step1. Import the required packages and print the present data.
step2.Find the null and duplicate values.
step3.Using logistic regression find the predicted values of accuracy , confusion matrices.
step4.Display the results.
```

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Sanjay K
RegisterNumber: 212223220094
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
### head
![image](https://github.com/SanjayBalaji0/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145533553/a1ddf9ac-987f-413e-9e1d-b1f4eb701291)
### head after dropping sl_no and salary
![image](https://github.com/SanjayBalaji0/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145533553/4cbe1341-7068-4673-b57b-7fd5a49dd0ab)
### isnull()
![image](https://github.com/SanjayBalaji0/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145533553/ad3d675c-b756-4625-a35c-b688cd8385e0)
### duplicated().sum()
![image](https://github.com/SanjayBalaji0/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145533553/05f7731b-1526-4a5f-89ae-e289ed729e49)
### data1
![image](https://github.com/SanjayBalaji0/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145533553/135e89f6-649f-4960-8096-3b1c498b5e3d)
### X
![image](https://github.com/SanjayBalaji0/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145533553/503a0d02-9a5c-4414-97e5-f4d7ab095144)
### Y
![image](https://github.com/SanjayBalaji0/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145533553/eac0513a-7d91-4215-85e2-04e9678f38b6)
### Y_pred
![image](https://github.com/SanjayBalaji0/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145533553/f04cc7ea-233a-4a2a-9e01-8be72732b26c)
### accuracy
![image](https://github.com/SanjayBalaji0/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145533553/03b4af28-c99a-42eb-927c-376aaebf3866)
### classification report
![image](https://github.com/SanjayBalaji0/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145533553/14fc1bad-f245-4531-971d-282c049711d1)
### Predict
![image](https://github.com/SanjayBalaji0/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145533553/4b0e911d-9017-488e-88bc-903791e5a413)



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
