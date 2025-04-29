<H3>ENTER YOUR NAME</H3>
<H3>ENTER YOUR REGISTER NO.</H3>
<H3>EX. NO.1</H3>
<H3>DATE</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:

##  PROGRAM:

## Import Libraries
```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

```
## Read the dataset
```
df=pd.read_csv("Churn_Modelling.csv")
df
```
## Checking Data
```
df.head()
df.tail()
df.columns
```
## Check the missing data
```
df.isnull().sum()
```
## Check for Duplicates
```
df.duplicated()
Assigning Y
y = df.iloc[:, -1].values
print(y)
```
## Check for Duplicates
```
df.duplicated()
```
## Check for outliers
```
df.describe()
```
## Dropping string values data from dataset
```
data = df.drop(['Surname', 'Geography','Gender'], axis=1)
```
## Checking datasets after dropping string values data from dataset
```
data.head()
```
## Normalize the dataset
```
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)
```
## Split the dataset
```
X=df.iloc[:,:-1].values
y=df.iloc[:,-1].values
print(X)
print(y)
```
## Training and testing model
```
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
print("X_train\n")
print(X_train)
print("\nLenght of X_train ",len(X_train))
print("\nX_test\n")
print(X_test)
print("\nLenght of X_test ",len(X_test))
```
## OUTPUT:
## Data
![image](https://github.com/user-attachments/assets/d861bfce-17ba-4f27-b49f-be9aa85c1b7a)
## Data Checking
![image](https://github.com/user-attachments/assets/eee31055-b964-4d20-a01c-2bc633ff2577)
## Missing Data
![image](https://github.com/user-attachments/assets/b46f890b-02d7-460c-ac48-8ce3978eced7)
## Values of 'Y'
![image](https://github.com/user-attachments/assets/78bbba4c-f5a1-4f2b-ba29-b4b24310f38d)
## Outliers
![image](https://github.com/user-attachments/assets/c5e0cd48-bcd6-42a3-bdb5-b5d5823ce3cf)
## Checking datasets after dropping string values data from dataset
![image](https://github.com/user-attachments/assets/0b1feaee-e870-4e88-9fba-ce80ae09a34e)
## Normalize the dataset
![image](https://github.com/user-attachments/assets/27aa93d5-a920-4e24-a850-ddd5e22ea0aa)
## Split the dataset
![image](https://github.com/user-attachments/assets/8195b084-5d20-4ca8-b6d5-af337776a919)
## Training and testing model
![image](https://github.com/user-attachments/assets/6f8fd84e-7dea-4833-bc00-617881fa9776)


## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


