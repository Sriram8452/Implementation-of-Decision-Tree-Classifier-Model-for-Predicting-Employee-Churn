# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

1. Import pandas library to read csv or excel file.
2. Import LabelEncoder using sklearn.preprocessing library.
3. Transform the data's using LabelEncoder.
4. Import decision tree classifier from sklearn.tree library to predict the values.
5. Find accuracy.
6. Predict the values.
7. End of the program.

## Program:
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

Developed by: Sriram G

RegisterNumber: 212222230149

```
import pandas as pd
data=pd.read_csv("Employee (1).csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data ["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
print(accuracy)
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

## Output:

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/9863ba0f-6dc6-48b9-b6ee-53380f1938cb)

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/b823b527-9080-4d47-8144-a75f11b8ff33)

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/54c501c3-b063-4edf-87e0-4cd709f01af0)

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/ac85c899-5d60-4240-9b88-fb1bd318fbc6)


![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/593863a0-b603-4058-8342-04e8ed200f6f)



![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/59c9d6c2-7088-4ea2-8ddd-cd183ebf4034)

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/6f2ccedb-a907-4191-ac4c-ab9f1efe5771)






## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
