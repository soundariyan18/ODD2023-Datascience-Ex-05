# Ex:05 Feature Generation

## AIM:

To read the given data and perform Feature Generation process and save the data to a file.

## EXPLANATION:

Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

## ALGORITHM:

STEP 1

Read the given Data

STEP 2

Clean the Data Set using Data Cleaning Process

STEP 3

Apply Feature Generation techniques to all the feature of the data set

STEP 4

Save the data to the file

Developed by: soundariyan 

reg: 212222230146


## PROGRAM:
```
import pandas as pd
from scipy import stats
import numpy as np

df=pd.read_csv("/content/bmi.csv")

from sklearn.preprocessing import StandardScaler
sc=StandardScaler()
df[['Height','Weight']]=sc.fit_transform(df[['Height','Weight']])
df.head(10)

import pandas as pd
df=pd.read_csv("/content/Encoding Data (1).csv")

from sklearn.preprocessing import LabelEncoder,OrdinalEncoder

temp=["Cold","Warm","Hot"]

enc=OrdinalEncoder(categories=[temp])

df["ord_2"]=enc.fit_transform(df[["ord_2"]])
df

from sklearn.preprocessing import OneHotEncoder

ohe=OneHotEncoder(sparse=False)
ohe.fit_transform(df[["nom_0"]])

df=pd.read_csv("/content/bmi(1).csv")

from sklearn.preprocessing import MinMaxScaler
mms=MinMaxScaler()
df=pd.DataFrame(mms.fit_transform(df),columns=['Height','Weight','Index'])
df

from sklearn.preprocessing import MaxAbsScaler
mas=MaxAbsScaler()
df=pd.DataFrame(mas.fit_transform(df),columns=['Height','Weight','Index'])
df

from sklearn.preprocessing import RobustScaler
rs=RobustScaler()
df=pd.DataFrame(rs.fit_transform(df),columns=['Height','Weight','Index'])
df
```

## OUTPUT:

![MODEL](https://user-images.githubusercontent.com/121222763/272937238-cb5339d6-d0c8-451e-9892-d67d3973888c.png)

![MODEL](https://user-images.githubusercontent.com/121222763/272939326-5ad23f86-e352-4aa2-a947-7e6f74c6fd32.png)

![MODEL](https://user-images.githubusercontent.com/121222763/272939683-f35107b7-61a9-4504-ab31-37631939a078.png)

![MODEL](https://user-images.githubusercontent.com/121222763/272939939-8352a24d-b87d-4eac-b14b-e6851d0c8e72.png)

![MODEL](https://user-images.githubusercontent.com/121222763/272939939-8352a24d-b87d-4eac-b14b-e6851d0c8e72.png)

![MODEL](https://user-images.githubusercontent.com/121222763/272940177-fee61260-15b8-49ff-8871-398abeb5bc14.png)

## RESULT:

Feature Generation process and Feature Scaling process is applied to the given data frames sucessfully.
