# Ex.No.6-Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

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
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Sriram G
RegisterNumber: 212222230149
*/
```

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

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/82383357-bc11-4984-a9fb-047e903eb7ee)

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/76e57ea7-1d7d-41ab-ac5f-e8b55bbfb811)

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/83c7b0ff-1a0b-4600-a2db-4ab7b928cebc)

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/51f2cca4-b719-47e4-afbc-3e35626ac93b)

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/b4fb5d4f-1fae-4092-968d-580f196a1da0)

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/1cf6b976-f20d-4fc6-8541-1d1120040db1)

![image](https://github.com/Sriram8452/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118708032/f9383146-25ca-4342-a747-1a5d3cdf1e1b)







## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
