# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 19/8/2026

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import matplotlib.pyplot as plt
import pandas as pd 
df=pd.read_csv("/content/TS001-Air_Passengers.csv")
df.head()
df['Date']=pd.to_datetime(df['Date'])
df.dtypes
df.set_index('Date',inplace=True)
df_resampled = df['#Passengers'].resample('D').interpolate()

df_resampled.plot(kind='line',label='Total Sales', color='black')
plt.title('Time Series Plot of Number of passengers ecah day')
plt.xlabel('Day')
plt.ylabel('Number of passengers')
plt.legend()
plt.grid(True)
plt.show()
```
# OUTPUT:
<img width="718" height="561" alt="Screenshot 2026-08-19 113313" src="https://github.com/user-attachments/assets/9683c519-f3ce-4eba-a64a-2e3d068f9221" />







# RESULT:
Thus we have created the python code for plotting the time series of given data.
