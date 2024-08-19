# Assignment-lab-intro-DS
# NAME: DHARSHINIYAA KS
# DEPT: CSE (CS)
# AIM:
To write a python program for inserting columns, rows and changing these etc.
# PROGRAM AND OUTPUT:
```
import pandas as pd
mydataset ={
    'cars':["BMW","Volvo","Ford"],'passings':[3,7,2]
}
myvar = pd.DataFrame(mydataset)
print(myvar)

import pandas as pd
data=[1,2,3,4]
df= pd.DataFrame(data)
print(df)

import pandas as pd
data={'name':['Alice','Bob','Dave','Emily'],'age':[24,30,40,45],'salary':[50000,60000,90000,70000]}
df=pd.DataFrame(data)
top_salary=df.nlargest(2,columns='salary')
print(top_salary)

import pandas as pd
data={'name':['Alice','Bob','Dave','Emily'],'age':[24,30,40,45],'gender':['F','M','M','F'],'height':['5.2','5.3','5.5','6.1']}
df=pd.DataFrame(data)
df=df.query('age >= 30')
print(df)

import pandas as pd
data={'name':['Alice','Bob','Dave','Emily'],'age':[24,30,40,45],'gender':['F','M','M','F'],'height':['5.2','5.3','5.5','6.1']}
df=pd.DataFrame(data)
df=df.query('name.str.contains("i")')
print(df)

import pandas as pd
data={'name':['Alice','Bob','Dave','Emily'],'age':[24,30,40,45],'gender':['F','M','M','F'],'height':['5.2','5.3','5.5','6.1']}
df=pd.DataFrame(data)
df.loc[:,'age']

import pandas as pd
data={'name':['Alice','Bob','Dave','Emily'],'age':[24,30,40,45],'gender':['F','M','M','F'],'height':['5.2','5.3','5.5','6.1']}
df=pd.DataFrame(data)
df.loc[:,['name','age']

import pandas as pd
data={'name':['Alice','Bob','Dave','Emily'],'age':[24,30,40,45],'gender':['F','M','M','F'],'height':['5.2','5.3','5.5','6.1']}
df=pd.DataFrame(data)
df.iloc[:,0]

import pandas as pd
data={'name':['Alice','Bob','Dave','Emily'],'age':[24,30,40,45],'gender':['F','M','M','F'],'height':['5.2','5.3','5.5','6.1']}
df=pd.DataFrame(data)
df_filtered = df[df['age']>30]
print(df_filtered)

import pandas as pd
data={'name':['Alice','Bob','Dave','Emily'],'age':[24,30,40,45],'gender':['F','M','M','F'],'height':['5.2','5.3','5.5','6.1']}
df=pd.DataFrame(data)
df_filtered = df[df['name'].str.startswith(('A','C'))]
print(df_filtered)

import pandas as pd
data=[['alex',10],['bob',10]]
df=pd.DataFrame(data,columns=['Name','Age'])
print(df)

import pandas as pd
df=pd.DataFrame({"a":[1,2,3],"b":[2,3,4],"c":[4,5,6]},index=[1,2,3])
print(df)

import pandas as pd
data=[{'a':1,'b':2},{'a':3,'b':10,'c':20}]
df=pd.DataFrame(data)
print(df)

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
address=['chennai','erode']
df["Address"]=address
print(df)

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
address=['chennai','erode']
df["Address"]=address
print(df)
del df['Address']
print(df)

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
address=['chennai','erode']
df["Address"]=address
print(df)
del df['Address']
print(df)
df.drop(['height'],axis=1,inplace=True)
print(df)

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
address=['chennai','erode']
df["Address"]=address
print(df)
del df['Address']
print(df)
df.drop(['height'],axis=1,inplace=True)
print(df)
df.pop('name')
print(df)

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
address=['chennai','erode']
df["Address"]=address
print(df)
df.rename(columns={'Address':'place'},inplace=True)
print(df)

import pandas as pd
df=pd.DataFrame([[1,2],[3,4]],columns=['a','b'])
df2=pd.DataFrame([[5,6],[7,8]],columns=['a','b'])
df=pd.concat([df,df2])
print(df)

import pandas as pd
df1=pd.DataFrame([[1,2],[3,4]],columns=['a','b'])
df2=pd.DataFrame([[5,6],[7,8]],columns=['a','b'])
df=df1.append(df2)
print(df)

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
address=['chennai','erode']
df["Address"]=address
print(df)
df.drop(['height'],axis=1,inplace=True)
print(df)
df.pop('name')
print(df)

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
df.filter(like='eight')

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
df.filter(items=['name','qualification'])
df.filter(like='eight')
df.filter(regex='a|e',axis=1)
print(df)


import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
print(df.tail(2))

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
print(df.head(2))

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
df.info()

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE']}
df=pd.DataFrame(data)
df.describe()

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE'],'age':[5,10]}
df=pd.DataFrame(data)
df_sorted=df.sort_values(by='age',ascending=False)
print(df_sorted)

import pandas as pd
data={'name':['alice','bob'],'height':[5.2,5.5],'qualification':['BE','BE'],'salary':[75000,50000]}
df=pd.DataFrame(data)
grouped=df.groupby('name').mean()['salary']
print(grouped)

```
# RESULT:
Thus we performed our required program.
