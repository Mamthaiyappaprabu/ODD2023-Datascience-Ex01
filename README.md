# Ex-01_DS_Data_Cleansing :


## AIM :
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation :
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM :
### STEP 1 :
Read the given Data
### STEP 2 :
Get the information about the data
### STEP 3 :
Remove the null values from the data
### STEP 4 :
Save the Clean data to the file

# CODE :
##  NAME : MAMTHA I
## REG NO : 212222230076

### FOR DATA_SET :
```

import pandas as pd
import numpy as np
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('Data_set.csv')

df.info()

df.head()

df=df.dropna(subset=['show_name'])
df.head()

df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df.head()

df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].median())
df.head()

df=df.dropna(subset=['current_overall_rank'])
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].mean())
df.head()

```
 ### FOR LOAN_DATA SET :
 ```

import pandas as pd
import numpy as np
from google.colab import files

uploaded=files.upload()
df=pd.read_csv('Loan_data.csv')

df.info()

df.head()

df['Gender']=df['Gender'].fillna('Female')
df.head()

df['Dependents']=df['Dependents'].fillna(method='ffill')
df.head()

df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df.head()

df=df.dropna(subset=['LoanAmount'])
df.head()

df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].min())
df.head()

```
# OUTPUT :

### FOR DATA_SET :
![Screenshot 2023-08-26 114523](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/cef6a111-6e2c-4a24-8839-4cb31c06031a)

![Screenshot 2023-08-26 115446](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/4314df12-71a0-4e4a-bfa7-dcbc220d4806)


![Screenshot 2023-08-26 115501](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/c0a39240-cfc0-46b1-820b-33c41ac2b61a)


![Screenshot 2023-08-26 115517](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/8294d55d-7e08-4c6d-8a97-5d149f92cecc)

![Screenshot 2023-08-26 115533](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/03092240-36f2-4e3c-9786-3b33f6946839)


![Screenshot 2023-08-26 115548](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/dbcad50e-5a47-4975-9eef-363491becf8d)
![Screenshot 2023-08-26 115609](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/f6ee80f5-46fb-43f9-8044-d0d5c8ba83e5)

![Screenshot 2023-08-26 115632](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/7e14a4e7-abc8-43e7-9b44-4f27512bd4c7)


### FOR LOAN DATA_SET :
![Screenshot 2023-08-27 220501](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/2d60281e-db76-4299-a5e7-755dc30f206e)

![Screenshot 2023-08-27 220514](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/206a4604-6d75-4ca0-9bdb-7b5d0fdd6195)
![Screenshot 2023-08-27 220530](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/16250e1d-cfcb-4042-9123-77cb7d0703ab)
![Screenshot 2023-08-27 220540](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/4599ef35-829a-4220-bb99-4fc1b30b2814)
![Screenshot 2023-08-27 220548](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/d94b84df-86b3-4814-a82c-a75f969b0e54)
![Screenshot 2023-08-27 220557](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/5bd36fb8-7573-4488-8311-39e3b2ba1085)
![Screenshot 2023-08-27 220607](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/41a18f5f-864b-401c-a167-8a6754f4e96d)
![Screenshot 2023-08-27 220622](https://github.com/Mamthaiyappaprabu/ODD2023-Datascience-Ex01/assets/119393563/7822e33f-e634-4be7-98d0-fff30fc029b7)

# RESULT :
Thus,the given data is read,cleansed and the cleaned data is saved into the file.
