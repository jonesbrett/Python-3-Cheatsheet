<p align="center">
  <img src="img/Python-Cheat-Sheets.png" width="900" height="526" align="center" title="Pythion cheatsheet">
  
</p>

Wellcome to my Cheat Sheet page, this is work in progress to assist me and any others who may find it useful.

# Table of Content
- [Data Types](#data-types)
- [Data Structures](#data-structures)
  - [Lists](#lists)
    - [List Items](#list-items)
    - [Changing the values of a list](#changing-the-values-of-a-list)
    - [Duplicates are Allowed](#duplicates-are-allowed)
    - [Length of List](#length-of-list)
    - [List - Data Types](#list---data-types)
  - [Dictionaries](#dictionaries)
  - [Tuples](#tuples)
    - [Tuples with one item](#tuples-items)
    - [Changing the value of a tuple](#changing-the-values-of-a-tuple)
    - [Concatenating Tuples](#concatenating-tuples)
    - [Reversing Tuples](#reversing-tuples)
  - [Sets](#sets)

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





# Data Structures

There are four different types of Data Structure, Lists, Dictionaries, Tuples and Sets:

## Lists

Lists are used to store multiple items in a single value, Lists use [square brackets]:

```python
thislist = ['apple', 'banana', 'cherry']
print(thilist)
# 'apple', 'banana', 'cherry'
```
### List Items

List items are ordered, changable, and allow duplicate values. List items are indexed, 
the first item has an index of [0], the second item [1]:

```python
thislist = ['apple', 'banana', 'cherry']
print(thilist[0])
# 'apple'
```

### Changing the values of a list 

List are mutable, meaning that we can change them by, adding or removing items after they are created:.

```python
thislist = ['apple', 'banana', 'cherry']
newlist = thislist + ['orange']
print(newlist)
# ['apple', 'banana', 'cherry', 'orange']
```

### Duplicates are Allowed

List can have duplicate values:

```python
thislist = ['apple', 'banana', 'cherry', 'apple']
print(thislist)
# ['apple', 'banana', 'cherry', 'apple']
```

### Length of List

The len() function returns the length of the list:

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








## Tuples

A tuple is a collection which is ordered, indexed and immutable (they can not be changed):

```python
t = ('a','b','c')
t = 'a','b'.'c'     # Note tuples can be written without the brackets too.
```
### Tuples items

A tuple can also have a single item in them too, but it needs to have a comma after it:

```python
a = (1,)    # a is the tuple (1,)
a = (1)     # a is the value and not a tuple

a = 1,    # a is the tuple (1,)
a = 1     # a is the value and not a tuple
```
### Changing the values of a tuple

Changing the values of tuples, can only be done if you convert the tuple to a list first and
then back to a tuple afterwards:

```python
colours = ('red','green','black')
newcolours = list(colours)
newcolours[2] = 'blue'
colours = tuple(newcolours)
print(colours)
# ('red', 'green', 'blue')
```
### Concatenating Tuples

You can Concatenate tuples useing the + sign:

```python
tuple1 = ('1','2','3')
tuple2 = ('a','b','c')

output = tuple1 + tuple2
print(output)
# '1','2','3','a','b','c'
```
### Reversing Tuples

Reversing the order of tuple:

```python
colours = ('red','green','blue')
rev = colours[::-1]
# rev: ('blue','green','red')
colours = rev
# colours: ('blue','green','red')
```
### The Max() and Min() function

The max() and min() functions in tuples:

```python
tuple1 = ('1','2','3')
max(tuple1)
# 3
min(tuple1)
# 1
```
### Length of tuples

The len() function returns the length of the tuple:

```python
tuple1 = ('1','2','3')
len(tuple1)
# 3
```


