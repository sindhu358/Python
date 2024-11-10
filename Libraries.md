# NUMPY

```
import numpy as np

x = np.array(
[3,2,4],
)
y = ([5,3,9])
print(x.shape) #size,type of dimensionalarray
print(x.dtype) # datatype
print(np.dot(x,y))
print((x*y).sum())

```
output

```
(3,)
int64
57
57
```

EX

```
import numpy as np

x = np.array([
[3,2,4],
[24,33,22],
[34,45,55],
[1,2,3]])
y = ([5,3,9])
print(x.shape) #size,type of dimensionalarray
print(x.dtype) # datatype
print(np.dot(x,y)) # matrix multiplication
print((x*y).sum())

```

output

```
(4, 3)
int64
[ 57 417 800  38]
1312
```

EX

```
import numpy as np
arr1 = list(range(1000000))
arr2 = list(range(1000000,2000000))
x = np.array(arr1)
y = np.array(arr2)

result = 0
for x1,x2 in zip(x,y):
    result += x1*x2
print(result)

```

output

```
833332333333500000

```
EX

```
import numpy as np
arr1 = list(range(1000000))
arr2 = list(range(1000000,2000000))
x = np.array(arr1)
y = np.array(arr2)

result = np.dot(x,y)
print(result)

```

output

```
833332333333500000

```
EX

```

import numpy as np

x = np.array([
[3,2,4],
[24,33,22],
[34,45,55],
[1,2,3]])
y = ([5,3,9])
print(np.matmul(x,y))
print(x @ y)

```
output

```
[ 57 417 800  38]
[ 57 417 800  38]

```




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



