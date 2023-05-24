# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas as pd.
2. Obtain the information of the data.
3. Print the sum of null datas.
4. Using DecsionTreeClassifier imported from sklearn we get the accuracy.
5. Print the predicted values.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Meetha Prabhu
RegisterNumber:  212222240065
**
import pandas as pd
data=pd.read_csv("/content/Employee (1).csv")
**
**
print("Data:")
data.head()
**
**
print("Information of data:")
data.info()
**
**
print("Sum of null data:")
data.isnull().sum()
**
**
print("'Left' data:")
data["left"].value_counts()
**
**
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
**
**
print("Salary Data:")
data["salary"]=le.fit_transform(data["salary"])
data.head()
**
**
print("X data:")
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
**
**
y=data["left"]
**
**
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
**
**
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
**
**
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
print("Accuracy:")
accuracy
**
**
print("Predicted Value:")
dt.predict([[0.5,0.8,9,260,6,0,1,2]])

*/
```

## Output:
![image](https://github.com/Meetha22003992/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119401038/0d88b1c4-608e-4216-a90d-10d5f1c5326c)

![image](https://github.com/Meetha22003992/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119401038/ca3e3498-d4a9-4a97-b264-df8eb5019911)

![image](https://github.com/Meetha22003992/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119401038/9acbbaf0-f21e-4841-b6e4-bb17a1574947)

![image](https://github.com/Meetha22003992/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119401038/7a36eeb6-928c-4c33-afee-af2dfe17bbda)

![image](https://github.com/Meetha22003992/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119401038/295d9c9a-5eb6-4c4e-9825-50a2e46c4ea4)

![image](https://github.com/Meetha22003992/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119401038/01bd98b4-c828-4a47-ad64-2f5efd2362c2)

![image](https://github.com/Meetha22003992/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119401038/4a1b3f51-80d0-4139-91ce-8a652d23864c)

![image](https://github.com/Meetha22003992/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119401038/41bd26b2-5b97-4d80-8e2d-032d1444661a)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
