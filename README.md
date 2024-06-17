
# Input/Output:

**Print():**
  ```
syntax: print(value(s), sep= ‘ ‘, end = ‘\n’, file=file, flush=flush)
```

**F-string:**
```
  syntax: print(f"{val}for{val} is a portal for {val}.")
```

EX:
```
Geek = { 'Id': 112,
         'Name': 'Harsh'}

print(f"Id of {Geek['Name']} is {Geek['Id']}")
```
o/p:

```
Id of Harsh is 112
```

**end='\n':** 
\n provides new line after printing

EX:
```
name = "Alice"
age = 30
print("My name is", name, "and I am", age, "years old.", end=" ")
print("Nice to meet you!")
```
o/p:
```
My name is Alice and I am 30 years old. Nice to meet you!
```
**Sep:**
It is a separator between arguments to print the function

EX:
```
print("geeks","for",'geeks',sep= '&')
```

**Output: Format method:**

EX:
```
print('I love {} for "{}!"'.format('Geeks', 'Geeks'))

#using format() method and referring a position of the object
print('{0} and {1}'.format('Geeks', 'Portal'))

print('{1} and {0}'.format('Geeks', 'Portal'))

print(f"I love {'Geeks'} for \"{'Geeks'}!\"")

#using format() method and referring a position of the object
print(f"{'Geeks'} and {'Portal'}")
```
o/p:
```
I love Geeks for "Geeks!"
Geeks and Portal
Portal and Geeks
I love Geeks for "Geeks!"
Geeks and Portal
```

**Taking multiple inputs from user**

- Using Split() method
taking 2 inputs at a time

EX:
```
x,y = input("enter the 2 values\n").split()
print("sum:",x+y)
```
o/p:
```
enter the 2 values
1 2
sum: 12
```

- Using map() and split() method

  EX:
  ```
  x,y = map(float,input("Enter multiple values:\n").split())
  print("product:",x*y)
  ```
  o/p:
  ```
  Enter multiple values:
  2 3
  product: 6.0
  ```

  - Using list Comprehension

  EX:
  ```
  a = [int(a) for a in input("Enter multiple inputs\n").split()]
  print("Enter a value:",a)
  ```
  o/p:

  ```
  Enter multiple inputs
  12 45 66 11 33
  Enter a value: [12, 45, 66, 11, 33]
  ```
# DataTypes
- strings
- Booleans
- List
- Tuple
- Dictionary
- Set
- Arrays
- Type Casting
## String
A String is a data structure in Python Programming that represents a sequence of characters.
Strings are immutable

- Slicing
  [start : end]
- reverse string
  [::-1]
  -  Reverse the string using reversed and join builtin function and reversed function
    Syntax: separator_string.join(iterable)
  
  EX
   ```
    gfg = "geeksforgeeks"
    gfg = "".join(reversed(gfg))

    print(gfg)
    ```
   EX
  
  ```
  s = "Hello world"
  l1 = list(s)
  l1[2] = 'p'
  s1 = ''.join(l1)
  print(s1)
  ```
  
  o/p:
  
  ```
  Heplo world
  ```
- split a string

```
line = "Geek1 \nGeek2 \nGeek3"
print(line.split())
print(line.split(' ', 1))
```

o/p:

```
['Geek1', 'Geek2', 'Geek3']
['Geek1', '\nGeek2 \nGeek3']
```

## Boolean
- AND (Both should be TRUE)
- OR (Any one should be True)
- NOT 
- ==(equivalent)
- =!(Not equivalent)
- IN
- IS
## List
It is mutable and a collection of no.of strings, floats,etc. and is represented by [].

EX:

```
Var = 'GEEKS FOR GEEKS'
B = str.split(Var)
print(B)
```
o/p:

```
['GEEKS', 'FOR', 'GEEKS']
```

- len() is used to get the length of list
- insert()- insert(position,value)
- append(),extend() - Adds element at the end of the list
- pop() - it removes last element of the list by default

- reverse() - Reverse the elements in the list
- reversed() - The reversed() function returns a reverse iterator, which can be converted to a list using the list() function.
- remove() - Remove method in List will only remove the first occurrence of the searched element.

### List Comprehension
syntax:

```
newList = [ expression(element) for element in oldList if condition ]
```

```
odd = [x**2 for x in range(2,11) if x % 2 ==1]
print(odd)
```

o/p:

```
[9, 25, 49, 81]
```

## Tuples
It is immutable. Iterations in tuples is faster than lists for speed of execution and are represented by ().

- count() - It will count the no.of occurence of a number
- Index() - Find in the tuple and returns the index of the given value where it’s available

## Set
It is collection of unique elements.They can be useful for removing duplicates from a collection of data.

```
syntax: s = {1,"s",1.5}
```
## Dictionary
These are represented by {key:value}
where keys cannot be changed or repeated.Keys are immutable.
  values can be changed or duplicated
- get() method is used for accesing the elements in the dict
    ```
    dict = {1: "geeks",2:2, 3: "for"}
    print(dict.get(3))
    ```

    o/p:

    ```
    for

    ```


EX:
```
dict1 = {1: "Python", 2: "Java", 3: "Ruby", 4: "Scala"}
dict2 = dict1.copy()
print(dict2)
dict1.clear()
print(dict1)
print(dict2.get(1))
print(dict2.items())
print(dict2.keys())
dict2.pop(4)
print(dict2)
dict2.popitem()
print(dict2)
dict2.update({3: "Scala"})
print(dict2)
print(dict2.values())
```

o/p:

```
{1: 'Python', 2: 'Java', 3: 'Ruby', 4: 'Scala'}
{}
Python
dict_items([(1, 'Python'), (2, 'Java'), (3, 'Ruby'), (4, 'Scala')])
dict_keys([1, 2, 3, 4])
{1: 'Python', 2: 'Java', 3: 'Ruby'}
{1: 'Python', 2: 'Java'}
{1: 'Python', 2: 'Java', 3: 'Scala'}
dict_values(['Python', 'Java', 'Scala'])
```







  

    
  
  

 










