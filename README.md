# EX.NO: 01 PLOT A TIME SERIES DATA...

###  DATE : 26/02/24 

## AIM :

To Develop a python program to Plot a time series data (population/ market price of a commodity/temperature) .

## ALGORITHM :

1. Import the required packages like pandas and matplot.
   
2. Read the dataset using the pandas.
 
3. Calculate the mean for the respective column.
   
4. Plot the data according to need and can be altered monthly, or yearly.
   
5. Display the graph.

## PROGRAM :

### Population Time Series Data :

```python

#dataset: https://fred.stlouisfed.org/series/POPTHM
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df["2017-01"]
df["2017"].mean()
df["2017-05":"2017-06"]
df.resample('Y').mean()
mean=df.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population(in Thousands)")
plt.show()

```

### Market Price of a Commodity Time Series Data :

```python

import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df["2017-01"]
df["2017-01"].Close.mean()
df["2017-05-01":"2017-08-31"]
df.Close.resample('M').mean()
df.Close.plot(kind='line')
plt.xlabel("Date")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()

```

### Temperature Time Series Data :

```python

import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("ClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
df["2017-01"]
df["2017"].mean()
df["2017-05-01":"2015-08-31"]
df['meantemp'].resample('M').mean()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
mean=df["meantemp"].resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Temperature")
plt.show()

```

## OUTPUT :

### Population Time Series Data :

![img1](https://github.com/anto-richard/TSA_EXP1/assets/93427534/d501904b-85dd-416a-9d12-0ce1f61ca5a6)

### Market Price of a Commodity Time Series Data :

![img2](https://github.com/anto-richard/TSA_EXP1/assets/93427534/405179e0-c274-4e97-b8f9-c1763480cd42)

![img3](https://github.com/anto-richard/TSA_EXP1/assets/93427534/457dddd0-6b24-46cf-af7d-4f973141ec05)

![img4](https://github.com/anto-richard/TSA_EXP1/assets/93427534/151a1d56-c5ff-452e-854c-7a3c873b6b8f)

### Temperature Time Series Data :

![img5](https://github.com/anto-richard/TSA_EXP1/assets/93427534/914f2636-835b-4587-85b5-6275ac59b18c)

![img6](https://github.com/anto-richard/TSA_EXP1/assets/93427534/ee1f81da-d4d9-4466-8c96-679eea34f83d)

## RESULT :

Thus, we have created the python code for plotting the time series of given data.
