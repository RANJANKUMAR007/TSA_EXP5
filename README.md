# Ex.No: 05  IMPLEMENTATION OF TIME SERIES ANALYSIS AND DECOMPOSITION
### Date:22/09/2025 


### AIM:
To Illustrates how to perform time series analysis and decomposition on the monthly average temperature of a city/country and for airline passengers.

### ALGORITHM:
1. Import the required packages like pandas and numpy
2. Read the data using the pandas
3. Perform the decomposition process for the required data.
4. Plot the data according to need, either seasonal_decomposition or trend plot.
5. Display the overall results.

### PROGRAM:
```
mport pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from statsmodels.tsa.seasonal import seasonal_decompose
```
```
data = pd.read_csv('gold_price_data.csv', parse_dates=['Date'], index_col='Date')
```
```
decomposition = seasonal_decompose(data_monthly, model='additive', period=12)

```
```
plt.figure(figsize=(10, 12))
```
```
plt.subplot(411)
plt.plot(data_monthly, label='Monthly Average Value')
plt.legend(loc='upper left')
plt.title('Original Gold Prices (Monthly Average)')
```
```
plt.subplot(412)
plt.plot(decomposition.trend, label='Trend', color='orange')
plt.legend(loc='upper left')
plt.title('Trend')
```
```
plt.subplot(413)
plt.plot(decomposition.seasonal, label='Seasonal', color='green')
plt.legend(loc='upper left')
plt.title('Seasonality')
```
```
plt.subplot(414)
plt.plot(decomposition.resid, label='Residual', color='red')
plt.legend(loc='upper left')
plt.title('Residuals')
```
```
plt.tight_layout()
plt.show()
```
### OUTPUT:
FIRST FIVE ROWS:
<img width="352" height="52" alt="image" src="https://github.com/user-attachments/assets/bfbacc13-b0ef-4e7f-a609-c6f4748c44eb" />

PLOTTING THE DATA:
<img width="526" height="165" alt="image" src="https://github.com/user-attachments/assets/6816385a-8fb0-47d9-b0b0-3a6776036424" />


SEASONAL PLOT REPRESENTATION :
<img width="648" height="191" alt="image" src="https://github.com/user-attachments/assets/9452e3c4-0b70-4fd0-88dd-71bc1fef757e" />

TREND PLOT REPRESENTATION :
<img width="657" height="197" alt="image" src="https://github.com/user-attachments/assets/16de83e7-82ee-408b-b4d9-158e30b8d32c" />

OVERAL REPRESENTATION:
<img width="777" height="242" alt="image" src="https://github.com/user-attachments/assets/9105d918-0098-4c3e-ae57-801e5538b793" />



### RESULT:
Thus we have created the python code for the time series analysis and decomposition.
