# Ex-03EDA

## AIM:
To perform EDA on the given data set. 

# Explanation:
The primary aim with exploratory analysis is to examine the data for distribution, outliers and 
anomalies to direct specific testing of your hypothesis.
 

# ALGORITHM:
###STEP 1:
     Import the required packages(pandas,numpy,seaborn).

###STEP 2:
     Read and Load the Dataset.

###STEP 3:
     Remove the null values from the data and remove the outliers.

###STEP 4:
     Remove the non numerical data columns using drop() method.

###STEP 5:
     returns object containing counts of unique values using (value_counts()).

###STEP 6:
     Plot the counts in the form of Histogram or Bar Graph.

###STEP 7:
     find the pairwise correlation of all columns in the dataframe(.corr()).

###STEP 8:
    Save the final data set into the file.

# CODE:
```
import pandas as pd
import numpy as np
import seaborn as np
df=pd.read_csv("titanic_dataset.csv")
df.info()
df.head(10)
df.isnull().sum()
df.drop("Cabin",axis=1,inplace=True)
df.info()
df.isnull().sum()
df["Age"] = df["Age"].fillna(df["Age"].median())
df.boxplot()
df.isnull().sum()
df["Embarked"] = df["Embarked"].fillna(df["Embarked"].mode()[0])
df.isnull().sum()
df.boxplot()
df["Embarked"].value_counts()
df["Pclass"].value_counts()
df["Survived"].value_counts()
np.countplot(x="Survived",data=df)
np.countplot(x="Pclass",data=df)
np.countplot(x="Sex",data=df)
df.info()
np.displot(df["Fare"])
np.countplot(x="Pclass",hue="Survived",data=df)
np.countplot(x="Sex",hue="Survived",data=df)
np.displot(df[df["Survived"]==0]["Age"])
np.displot(df[df["Survived"]==1]["Age"])
pd.crosstab(df["Pclass"],df["Survived"])
pd.crosstab(df["Sex"],df["Survived"])
df.corr()
np.heatmap(df.corr(),annot=True)
```


# OUPUT:
![output](./Ex.3.ds1.PNG)
![output](./Ex.3.ds2.PNG)
![output](./Ex.3.ds3.PNG)
![output](./Ex.3.ds4.PNG)
![output](./Ex.3.ds5.PNG)
![output](./Ex.3.ds6.PNG)
![output](./Ex.3.ds7.PNG)
![output](./Ex.3.ds8.PNG)
![output](./Ex.3.ds9.PNG)
![output](./Ex.3.ds10.PNG)
![output](./Ex.3.ds11.PNG)
![output](./Ex.3.ds12.PNG)
![output](./Ex.3.ds13.PNG)
![output](./Ex.3.ds14.PNG)
![output](./Ex.3.ds15.PNG)
![output](./Ex.3.ds16.PNG)
![output](./Ex.3.ds17.PNG)
![output](./Ex.3.ds18.PNG)
![output](./Ex.3.ds19.PNG)
![output](./Ex.3.ds20.PNG)
![output](./Ex.3.ds21.PNG)
![output](./Ex.3.ds22.PNG)
![output](./Ex.3.ds23.PNG)
![output](./Ex.3.ds24.PNG)
![output](./Ex.3.ds25.PNG)