# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import chardet

2. Read the dataset

3. Import SVC from sklearn

4. Fit the data in the model and run the algorithm

## Program:

/*
Program to implement the SVM For Spam Mail Detection..


## Developed by: R.SUBHASHRI
## RegisterNumber:212223230219


```

import chardet
file='/content/spam.csv'
with open(file,'rb') as rawdata:
    result=chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv("/content/spam.csv",encoding='Windows - 1252')

data.head()

data.info()

data.isnull().sum()

x=data['v1'].values
y=data['v2'].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy



```



  





### RESULT OUTPUT

![image](https://github.com/Sachin-vlr/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497666/7fc28e96-c69c-425f-aa26-bbd633dd44c0)

### DATA.HEAD()




![image](https://github.com/Sachin-vlr/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497666/747c9703-064a-4fbd-9f09-c685c2339df9)

### DATA.INFO()

![image](https://github.com/Sachin-vlr/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497666/09533dd4-7f5e-4493-9cba-35091a46d7d1)

### DATA.ISNULL().SUM()


![image](https://github.com/Sachin-vlr/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497666/04619be3-255a-40cf-a6a7-5009c4a7820e)


### Y_PREDICTION VAUE


![image](https://github.com/Sachin-vlr/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497666/0bbcc78e-5645-4e4f-91f4-e584ea372e7f)

### ACCURACY VALUE

![image](https://github.com/Sachin-vlr/Implementation-of-SVM-For-Spam-Mail-Detection/assets/113497666/bf4518d1-2af2-4b8e-a582-bbd3b4178d41)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
