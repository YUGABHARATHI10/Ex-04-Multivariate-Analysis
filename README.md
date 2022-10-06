# Ex-04-Multivariate-Analysis

AIM:

To apply multivariant analysis on the given data set.

ALGORITHM:

1.start

2.read the dta from the file

3.clean the data a)remove outliers b)fill the null value or drop the column

4.perform multivariate analysis a)scatter plot b)box plot c)heat map

Developed by : SS YUGABHARATHI

Registration Number : 212220040183
CODE:

ISNULL.SUM():


![1](https://user-images.githubusercontent.com/95409048/192733644-a78fc354-c4f3-4ad1-a8cb-b88100f9930b.png)

DTTYPES:

![2](https://user-images.githubusercontent.com/95409048/192734095-fcca8e32-75d2-4b76-aebf-38213cb2fe7b.png)

KURTOSIS:

![3](https://user-images.githubusercontent.com/95409048/192734186-2dc2bc8d-7dc7-4775-84ee-cbbe5c8e89d3.png)

BOX PLOT:

![4](https://user-images.githubusercontent.com/95409048/192734315-f72e5044-6054-4fdb-aedb-8d63ac261762.png)

BARPLOT:

![5](https://user-images.githubusercontent.com/95409048/192734419-b911880d-bdfe-421c-bdb5-040c609d1ae2.png)

CODE:

import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

states=df.loc[:,["Postal Code","Sales"]]

states=states.groupby(by=["Postal Code"]).sum().sort_values(by="Sales")

plt.figure(figsize=(17,7))

sns.barplot(x=states.index,y="Sales",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Postal Code")

plt.ylabel=("Sales")

plt.show()

![6](https://user-images.githubusercontent.com/95409048/192734667-61668901-a16e-40c2-bd66-20d775f9300d.png)

CODE:

import pandas as pd

import seaborn as sns 

import matplotlib.pyplot as plt

states=df.loc[:,["State","Postal Code"]]

states=states.groupby(by=["State"]).sum().sort_values(by="Postal Code")

plt.figure(figsize=(17,7))

sns.barplot(x=states.index,y="Postal Code",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Sales")

plt.ylabel=("Postal Code")

plt.show()

![7](https://user-images.githubusercontent.com/95409048/192735036-3d5e6620-6e41-401f-9192-dd33f7fd73e5.png)

![8](https://user-images.githubusercontent.com/95409048/192735092-22b6f664-068f-4757-8c9c-55edb3069e81.png)

CODE:

import numpy as np

import seaborn as sn

import matplotlib.pyplot as plt

data=pd.read_csv("/content/SuperStore.csv")

data = np.random.randint(low = 1, high = 100, size = (10, 10))

print("The data to be plotted:\n")

print(data)

hm = sn.heatmap(data = data)

plt.show()

![9](https://user-images.githubusercontent.com/95409048/192735217-0c4e8d82-0b6f-4ba1-b604-332e2e4eba75.png)


