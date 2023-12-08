import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
Data = pd.read_csv('D:\LoyersMaisons.csv' , delimiter = ';')
Data
plt.scatter (Data['surface'],Data['loyer'],color='red')
Data = Data[Data['loyer']<=10000]
Data
plt.scatter (Data['surface'],Data['loyer'],color='red')
x=Data.iloc[ : , :-1 ].values
y=Data.iloc[ : , -1].values
y
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2)
len(x)
len(x_train)
len(x_test)
regressor = LinearRegression()
regressor.fit(x_train,y_train)
y_pred = regressor.predict(x_test)
y_pred
regressor.predict([[44]])
regressor.predict([[70]])
plt.scatter(x_test,y_test,color='red')
plt.plot(x_train,regressor.predict(x_train),color='blue')
plt.title('Evolution des loyers par surface')
