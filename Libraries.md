# NUMPY

**EX-shape,dtype, dot notation**

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

**EX- range **

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
**EX- matrix multiplication**

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
numpy.concatenate() function concatenate a sequence of arrays along an existing axis.

**EX- Concatenate**

```
import numpy as np
x = np.array([
[3,2,4],[2,1,4]])
y = ([[5,3,9],[3,1,4]])
new = np.concatenate((x,y))
print(new)

```
OUTPUT

```
[[3 2 4]
 [2 1 4]
 [5 3 9]
 [3 1 4]]

```

**EX-reshape**

```

import numpy as np

x = np.array([[3,2,4],[2,1,4],[1,3,5],[1,3,5]])
new = np.reshape(x, (2,3,2)) # depth,rows,columns
print(new)

```

op

```
[[[3 2]
  [4 2]
  [1 4]]

 [[1 3]
  [5 1]
  [3 5]]]

```
**EX : Reshape**

```

import numpy as np

x = np.array([[3,2,4],[2,1,4],[1,3,5],[1,3,5]])
three_D = np.reshape(x, (2,3,2))# size,rows,col
two_D = np.reshape(x,(2,6))# rows,col
negative = np.reshape(x,(6,-1)) # -1 will automatically sets the column ratio

print("The 3_D array is :",three_D,)
print("The 2_D array is:",two_D)
print("The array that sets itself:",negative)

```
OP

```
The 3_D array is : [[[3 2]
  [4 2]
  [1 4]]

 [[1 3]
  [5 1]
  [3 5]]]
The 2_D array is: [[3 2 4 2 1 4]
 [1 3 5 1 3 5]]
The array that sets itself: [[3 2]
 [4 2]
 [1 4]
 [1 3]
 [5 1]
 [3 5]]

```

**EX - SLicing and indexing**

```


import numpy as np
x = np.array([[[11,12,13,14],
                [13,14,15,19]],
                
                [[15,16,17,21],
                [63,92,36,18]],
                
                [[98,32,81,23],
                [17,18,19.5,43]]])
print(x.shape) #size of array
Y1 = x[1,1,3]
print("The sinlge element is:",Y1) 
Y2 = x[1:,0:1,:2]
print("subarray using ranges:",Y2)
Y3 = x[1:,1,:3]
print("mix of indices and ranges:",Y3)
Y4 = x[1]
print("mix of fewer indices:", Y4)
Y5 = x[:2,1]
print("Using fewer indices:",Y5)

```
Output:

```

(3, 2, 4)
The sinlge element is: 18.0
subarray using ranges: [[[15. 16.]]

 [[98. 32.]]]
mix of indices and ranges: [[63.  92.  36. ]
 [17.  18.  19.5]]
mix of fewer indices: [[15. 16. 17. 21.]
 [63. 92. 36. 18.]]
Using fewer indices: [[13. 14. 15. 19.]
 [63. 92. 36. 18.]]

```

Using too many indices like 

```

x[1,,3,21]

```
will give an error as it is exceeding the length of the array 

## Creating Numpy Arrays

EX

```

import numpy as np
x = np.zeros((3,2)) #null matrix
print("array of all zeros:",x)

y = np.ones((2,2,3))
print("arrays of all ones:\n",y)

z = np.eye(3)
print("array of identity matrix:\n",z)

l = np.random.rand(5) #picks the value from 0 to 1 
print("array of random vector\n",l)

a = np.random.randn(2,3) # picks the value from gaussian distribution
print("Array of random matrix\n",a)

b = np.full([2,3],42)# fixed value
print("Creting 2x3 matrix using a fixed value 42\n",b)

c = np.arange(10,90,3)#start,end,step
print("Range with start,end,step\n",c)

d = np.linspace(3,27,9)# start,end,length of numbers
print("Equally spaced in a range\n",d)

```
op

```
array of all zeros: [[0. 0.]
 [0. 0.]
 [0. 0.]]
arrays of all ones:
 [[[1. 1. 1.]
  [1. 1. 1.]]

 [[1. 1. 1.]
  [1. 1. 1.]]]
array of identity matrix:
 [[1. 0. 0.]
 [0. 1. 0.]
 [0. 0. 1.]]
array of random vector
 [0.09569455 0.13666593 0.31535523 0.54704971 0.4020648 ]
Array of random matrix
 [[-0.63285752  0.32999558 -0.91551673]
 [ 2.03932966 -0.39783963  1.21046526]]
Creting 2x3 matrix using a fixed value 42
 [[42 42 42]
 [42 42 42]]
Range with start,end,step
 [10 13 16 19 22 25 28 31 34 37 40 43 46 49 52 55 58 61 64 67 70 73 76 79
 82 85 88]
Equally spaced in a range
 [ 3.  6.  9. 12. 15. 18. 21. 24. 27.]

```
## OS module
The OS module in Python provides many functions interacting with the OS and the file system 

```
import OS

```
1.Check the present directory using the **os.getcwd** function
EX
```
import os
# Get current working directory
cwd = os.getcwd()
print("Current working directory:", cwd)

```
output

```
 C:/Users/user/AppData/Local/Programs/Python/Python312/python.exe c:/Users/user/Documents/numoy.py
Current working directory: C:\Users\user

```
EX
2.To get the list of the files in a directory, use **os.listdir**

```
import os
# Get current working directory
cwd = os.listdir()
print("Current working directory:", cwd)

```
op

```
PS C:\Users\user> & C:/Users/user/AppData/Local/Programs/Python/Python312/python.exe c:/Users/user/Documents/numoy.py
Current working directory: ['.arduinoIDE', '.dotnet', '.git', '.gitconfig', '.idlerc', '.ipynb_checkpoints', '.ipython', '.jupyter', '.lesshst', '.matplotlib', '.packettracer', '.ssh', '.templateengine', '.vscode', 'AppData', 'Apple', 'Application Data', 'battery-report.html', 'Cisco Packet Tracer 8.2.2', 'Contacts', 'Cookies', 'Desktop', 'Documents', 'Downloads', 'Favorites', 'GIT', 'IntelGraphicsProfiles', 'IOT', 'Links', 'Local Settings', 'Music', 'My Documents', 'NetHood', 'NTUSER.DAT', 'ntuser.dat.LOG1', 'ntuser.dat.LOG2', 'NTUSER.DAT{3ee1e3fe-5764-11ef-bdd8-004238c52871}.TM.blf', 'NTUSER.DAT{3ee1e3fe-5764-11ef-bdd8-004238c52871}.TMContainer00000000000000000001.regtrans-ms', 'NTUSER.DAT{3ee1e3fe-5764-11ef-bdd8-004238c52871}.TMContainer00000000000000000002.regtrans-ms', 'ntuser.ini', 'OneDrive', 'Pictures', 'PrintHood', 'Recent', 'Saved Games', 'Searches', 'SendTo', 'Start Menu', 'Templates', 'Videos']

```


os.listdir('.') # relative path, dot refers to the current directory 

```
os.listdir('./usr') # absolute path
```

```
os.listdir('./usr/bin)
````

A new directory can be created using **os.makedirs**.

using urllib module we can download some files to the created file

```
import urllib.request
urllib.request.urlretrieve(url1,"")
os.listdir(filename) # checks whether the files were downloaded to the required directory

```
To open a file we use a builtin function called as **open**
there are different types of modes as well
file1 is referred as an object
 ```
file1 = open("",mode = 'r')

```
To read the contents of the file we use the **read** method of the file object

```
file_contents = file1.read()
```

To close the file we use

```
file1.close()
```
### Closing files automatically using **with**
To automatically close a file once we are done with processing it, we can open it using with statement

```
with open("filename",'r')as file2:
    file2_contents = file2.read()
    print(file2_contents)
```
### Read a file line by line
readlines - File object which provide 

```
withopen("filename",'r') as file3:
    file3_lines = file3.readlines()
```
we will get an output of each line of the file with\n at the end of each line
In order to remove \n from each line we use **strip()** function
```
file3_lines[0].strip()
```
This will remove the newline character i.e., \n

#### Processing data from files

Before performing any operations on the data stored in a file, we need to convert the contents of the file one large string into Python data types.
For the file containing information about loans in CSV format, we can do the following:
1. Read the file line by line
2. Parse the first line to get list of the column anmes or headers
3. Split each remaining line and convert each value intlo float
4. create a dictionary for each value using headers as keys
5. create alist of dictionaries to keep track of all the loans

As we perform the same operations for multiple files, it would be useful define a function ``` read_csv ``` to do this. We will aslo define some helper functions to build up the functionality step by step.

``` parse_header ``` takes a line as input and returns a list of column headers.

```
def parse headers(header_line):
    return header_line.strip().split(',')
```

```
def parse_values(data_line):
    values = []
    for item in data_line.strip().split(','):
        if item == '':
            values.append(0.0)
        else:
            values.append(float(item))
    return values
```
Create a dictionary which takes a list of values and a list of headers as inputs and returns dictionary with the values and keys

```
def create_item_dict(values,headers):
    result = {}
    for value,headers in zip(value,header):
        result[header] = value
    return result
```

Now put it together and define a ```read_csv``` function

```
def parse headers(header_line):
    return header_line.strip().split(',')
def parse_values(data_line):
    values = []
    for item in data_line.strip().split(','):
        if item == '':
            values.append(0.0)
        else:
            values.append(float(item))
    return values
def create_item_dict(values,headers):
    result = {}
    for value,headers in zip(value,header):
        result[header] = value
    return result
def read_csv(path):
    result = []
    #Open the file in read mode
    with open(path, 'r') as f:
        # Get a lsit of lines
        lines = f.readlines()
        # parse the header
        headers = parse_headers(lines[0])
        #Loop over the remaining lines
        for data_line in lines[1:]:
            # Parse the values
            values = parse_values(data_line)
            # Create a dictionary using values and headers
            item,_dict = create_item_dict(values,headers)
            # Add the dictionary to tje result
            result.append(item_dict)
    return result

```
#### Writing to files
[= 













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



