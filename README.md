
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



 










