- [Return to Table of Contents](/../../)  

# Data Types                                                                                          

Data types are an important concept in programming. Variables store data of different types,
which can do different things. Python has the following data types:

| Description | Data Type |
| ----------- | --------- |
| Text Type | str |
| Numeric Type | int, float, complex |
| Sequence Type | list, tuple, range |
| Mapping Type | dict |
| Set Type | set, frozenset |
| Boolean Type | bool |
| Binary Types | bytes, bytearray, memoryview |
| None Types | NoneType |

### Getting the Data Type

You can get the data type of any object using the type() function:

```python
x = 5
print(type(x))
# <class 'int'>
```

### Setting the Specific Data Type

You can set the data type using the following constructors:

| Example | Data Type |
| ------- | --------- |
| x = str('Hello World') | str |
| x = int(20) | int | 
| x = floar(20.5) | float |
| x = complex(1j) | complex |
| x = list(('apple', 'banana', 'cherry')) | list | 
| x = tuple(('apple', 'banana', 'cherry')) | tuple |
| x = range(6) | range |
| x = dict(name='John', age=36) | dict |
| x = set(('apple', 'banana', 'cherry')) | set |
| x = frozenset(('apple', 'banana', 'cherry')) | frozenset |
| x = bool(5) | bool |
| x = bytes(5) | bytes |
| x = bytearray(5) | bytearray |
| x = memoryview(bytes(5)) | memoryview |



# Data Collections

There are four different types of Data Collections which are built into Python, Lists, Dictionaries, Tuples and Sets:

## Lists

Lists are used to store multiple items in a single value, Lists use [square brackets]:

```python
thislist = ['apple', 'banana', 'cherry']
print(thilist)

'apple', 'banana', 'cherry'
```
### List Items

List items are ordered, changable, and allow duplicate values. List items are indexed, 
the first item has an index of [0], the second item [1]:

```python
thislist = ['apple', 'banana', 'cherry']
print(thilist[0])

'apple'
```
You can also specify the reverse order of a List using a negative index, 
the last value would be [-1] and the second last [-2]:

```python
thislist = ['apple', 'banana', 'cherry']
print(thilist[-1])

'cherry'
```

### Changing the values of a List 

List are mutable, meaning that we can change them by, adding or removing items after they are created:

```python
thislist = ['apple', 'banana', 'cherry']
newlist = thislist + ['orange']
print(newlist)

['apple', 'banana', 'cherry', 'orange']
```

You can aslo use the '.append' method to add values to the end of a List:

```python
thislist = ['apple', 'banana', 'cherry']
thislist.append('orange')
print(thislist)

['apple', 'banana', 'cherry', 'orange']
```

Or you can use the '.insert' method to add values using indexing:

```python
thislist = ['apple', 'banana', 'cherry']
thislist.insert(1, 'orange')
print(thislist)

['apple', 'orange', 'banana', 'cherry']
```

Removing values from a List can be done using indexing:

```python
newlist = ['apple', 'banana', 'cherry', 'orange']
del newlist[0]
print(newlist)

['banana', 'cherry', 'orange']
```

### Duplicates are Allowed

List can have duplicate values:

```python
thislist = ['apple', 'banana', 'cherry', 'apple']
print(thislist)

['apple', 'banana', 'cherry', 'apple']
```

### Length of List

The len() function returns the length of the List:

```python
thislist = ['apple', 'banana', 'cherry', 'apple']
print(len(thislist))
# 4
```

### List - Data Types

List can be any type of data:

```python
list1 = ['apple', 'banana', 'cheery']   # String
list2 = [1, 2, 3, 4, 5]                 # Int
list3 = [True, False, False]            # Boolean
```
Lists can also be a combination of all data types:

```python
list = ['abc', 123, True]
```
>__Note__ You should use a List if the values are of a different type. In such cases Tuples are better to use.


### Mapping Data to a List

You can map data to multiple values in a List using the map funtion, for example if the user had entered 3 and 4:

```python
a, b = list(map(int, input("enter two digits").split()))
print(a + b)

7
```

### Sorting Lists

You can sort Lists with the '.sort()' method:

```python
thislist = ["cherry", "orange", "apple", "banana"]
thislist.sort()
print(thislist)

['apple', 'banana', 'cherry', 'orange']
```

You can reverse the sorted List using the '.sort(reverse=True)' method:

```python
thislist = ["cherry", "orange", "apple", "banana"]
thislist.sort(reverse=True)
print(thislist)

['orange', 'cherry', 'banana', 'apple']

# Note that when using the sort method, you can not un-sort once done.
```

To keep the original order in the List and sort the output, you use the 'sorted' function:

```python
thislist = ["cherry", "orange", "apple", "banana"]
print(sorted(thislist))

['apple', 'banana', 'cherry', 'orange']
```

### Copying Lists

List names are only reference points to the memory location of the List, so when you change the List,
it will effect both Lists:

```python
thislist = ["cherry", "orange", "apple", "banana"]
newlist = thislist
thislist.append('grape')
Print('Original:', thislist, '\nNewlist: ', newlist)

Original: ['cherry', 'orange', 'apple', 'banana', 'grape'] 
Newlist:  ['cherry', 'orange', 'apple', 'banana', 'grape']

# Note that both the Lists are the same.
```

To create a duplicate of the original List you need to use slicing:

```python
thislist = ["cherry", "orange", "apple", "banana"]
newlist = thislist[:]
thislist.append('grape')
Print('Original:', thislist, '\nNewlist: ', newlist)

Original: ['cherry', 'orange', 'apple', 'banana', 'grape'] 
Newlist:  ['cherry', 'orange', 'apple', 'banana']
```


## Tuples

A Tuple is a collection which is ordered, indexed and immutable (they can not be changed):

```python
t = ('a','b','c')
t = 'a','b','c'     # Note Tuples can be written without the brackets too.
```
### Tuples Items

A Tuple can also have a single item in them too, but it needs to have a comma after it:

```python
a = (1,)    # a is the Tuple (1,)
a = (1)     # a is the value and not a Tuple

a = 1,    # a is the Tuple (1,)
a = 1     # a is the value and not a Tuple
```
### Changing the values of a Tuple

Changing the values of tuples, can only be done if you convert the Tuple to a List first and
then back to a Tuple afterwards:

```python
colours = ('red','green','black')
newcolours = list(colours)
newcolours[2] = 'blue'
colours = tuple(newcolours)
print(colours)

('red', 'green', 'blue')
```
### Concatenating Tuples

You can Concatenate Tuples using the + sign:

```python
tuple1 = ('1','2','3')
tuple2 = ('a','b','c')

output = tuple1 + tuple2
print(output)

'1','2','3','a','b','c'
```
### Reversing Tuples

Reversing the order of Tuple:

```python
colours = ('red','green','blue')
rev = colours[::-1]
# rev: ('blue','green','red')
colours = rev
# colours: ('blue','green','red')
```
### The Max() and Min() function

The max() and min() functions in Tuples:

```python
tuple1 = ('1','2','3')
max(tuple1)
# 3
min(tuple1)
# 1
```
### Length of tuples

The len() function returns the length of the Tuple:

```python
tuple1 = ('1','2','3')
len(tuple1)
# 3
```

## Dictionaries

Dictionaries are used to store data values in key:value pairs. Dictionaries are written with {curly brackets}:

```python
thisdict = {'brand':'Ford', 'model':'Mustang', 'year':1964}
print(thisdict)

{'brand':'Ford', 'model':'Mustang', 'year':1964}
```

### Dictionary Items

A Dictionary is a collection which is ordered, changeable and do not all duplicates.

```python
thisdict = {'brand':'Ford', 'model':'Mustang', 'year':1964}
print(thisdict['brand'])

Ford
```

### keys and Values in Dictionaries

To view the key in a Dictionary you use the '.key()' methond:

```python
thisdict = {'brand':'Ford', 'model':'Mustang', 'year':1964}
for element in thisdict.keys():
    print(element)

brand
model
year
```
To view the values in a Dictionary you use the '.values()' methond:

```python
thisdict = {'brand':'Ford', 'model':'Mustang', 'year':1964}
for element in thisdict.values():
    print(element)

Ford
Mustang
1964
```
To view both the key and values in a dictionary you use the .item() method:

```python
thisdict = {"brand": "Ford", "model": "Mustang", "year": 1964}
for x, y in thisdict.items():
    print(x, y)

brand Ford
model Mustang
year 1964
```

## Sets

Sets are used to store multiple items in a single variable. Sets are a collection which are un-ordered,
un-indexed and does not allow duplicates. Sets do not support indexing, slicing or any other squence-like behavior.
Sets are written with {curly brackets}:

```python
thisset = {'aplle', 'banana', 'cheery'}
print(thisset)

{'cherry', 'apple', 'banana'} 
```

## Frozensets

Frozenset are immutable, therefore they can not be changed after creation.


- [Return to Table of Contents](/../../)
