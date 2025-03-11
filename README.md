# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date:11/03/2025

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.)
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
import pandas as pd
import matplotlib.pyplot as plt
file_path = "EURUSD.csv" 
data = pd.read_csv(file_path)
data.head()
data['Time']=pd.to_datetime(data['Time'])
data.set_index('Time',inplace=True)
plt.figure(figsize=(10,6))
plt.plot(data.index,data['Close'],label='EURUSD 2016-20',color='blue')
plt.title('EURUSD 2016-20')
plt.xlabel('Time')
plt.ylabel('Close')
plt.grid(True)
plt.legend()
plt.show()
# OUTPUT:
![time series-1](https://github.com/user-attachments/assets/467c9a38-f1b6-40d2-bc55-671b4549ba5e)
# RESULT:
Thus we have created the python code for plotting the time series of given data.
