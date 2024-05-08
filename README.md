# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.
2.Upload and read the dataset.
3.Check for any null values using the isnull() function.
4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.

## Program:
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: v.sanjay
RegisterNumber:  212223230188

import pandas as pd    
data=pd.read_csv("C:/Users/admin/Desktop/Employee.csv")    
data.head()     
data.info()    
data.isnull().sum()    
data['left'].value_counts()     
from sklearn.preprocessing import LabelEncoder    
le=LabelEncoder()    
data['salary']=le.fit_transform(data['salary'])    
data.head()     
x=data[['satisfaction_level','last_evaluation','number_project','average_montly_hours','time_spend_company','Work_accident','promotion_last_5years','salary']]     
x.head()    
y=data['left']     
from sklearn.model_selection import train_test_split    
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)    
from sklearn.tree import DecisionTreeClassifier    
dt=DecisionTreeClassifier(criterion='entropy')    
dt.fit(x_train,y_train)     
y_predict=dt.predict(x_test)     
from sklearn import metrics      
accuracy=metrics.accuracy_score(y_test,y_predict)     
accuracy      
dt.predict([[0.5,0.8,9,260,6,0,1,2]])    


## OUTPUT:

## data.head()

![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/149365143/f24f2a8c-3faf-4d64-8e2d-1da7ed2da290)
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
## data.info()

![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/149365143/652ad3b5-0784-43b3-9bbc-63a4ebca9d37)

## CHECKING NULL VALUES 

![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/149365143/a45d5c35-fbeb-4e9a-b4e7-9a782d9786f8)

## Value_counts()


![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/149365143/0abfc33d-7845-43d1-ab5f-796af8fcadfc)

## Dataset after encoding


![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/149365143/5b336a81-afb7-45d9-8b25-3b4d758f47d7)

## x values


![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/149365143/708cc013-2566-4fa3-8ee2-2f7966d0c3e4)

## Accuracy

![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/149365143/2a708ed5-7840-4798-a5b5-e8de117eec6b)

## dt.predict()


![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/149365143/08cb1f01-8812-4173-b1c5-379d5d380ba9)










## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
