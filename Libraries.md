# PANDAS
To manipulate data i.e., Tabular data such as spreadsheets or SQL tables
This is mainly used as input for plotting functions in **Matplotlib**, statistical analysis in Scipy,etc
* Data set cleaning, merging, joining, Inserting and deleting of columns from data frame. 
* Handling missing data in floating points and non-floating points
* Data visualization

Data Structures for manipulating data
1. Series
2. Data Frame

### Series:
One dimensional array capable of holding data of an integer, string , float ,Python Objects,etc..
It is nothing but a column in an Excel sheet.

**EX**

```
import pandas as pd 
import numpy as np

# Creating empty series 
ser = pd.Series() 
print("Pandas Series: ", ser) 

# simple array 
data = np.array(['g', 'e', 'e', 'k', 's']) 
  
ser = pd.Series(data) 
print("Pandas Series:\n", ser)
```

Output:

```
Pandas Series: Series([], dtype: float64)
Pandas Series:
0    g
1    e
2    e
3    k
4    s
dtype: object

````

w

