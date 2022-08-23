<p align="center">
  <img src="img/Python-Cheat-Sheets.png" width="900" height="526" align="center" title="Pythion cheatsheet">
  
</p>

Wellcome to my Cheat Sheets, this is work in progress to assist me and any others who may find it useful.

# Table of Content
- [Data Structures](#data-structures)
  - [Tuples](#tuples)

















## Tuples

A tuple is a collection which is ordered, indexed and immutable (they can not be changed):

```python
t = ('a','b','c')
t = 'a','b'.'c'     # Note Tuples can be written without the brackets too.
```
A tuple can also have a single item in too, but it need to have a comma after it:

```python
a = (1,)    # a is the tuple (1,)
a = (1)     # a is the value and not a tuple

a = 1,    # a is the tuple (1,)
a = 1     # a is the value and not a tuple
```
Changing the values of tuples, this can only be done if you convert the tuple to a list first and
then back to a tuple afterwards:

```python
colours = ('red','green','black')
newcolours = list(colours)
newcolours[2] = 'blue'
colours = tuple(newcolours)
print(colours)
# ('red', 'green', 'blue')
```
You can Concatenate tuples useing the + sign:

```python
tuple1 = ('1','2','3')
tuple2 = ('a','b','c')

output = tuple1 + tuple2
print(output)
'1','2','3','a','b','c'
```
Reversing the order of tuple

```python
colours = ('red','green','blue')
rev = colours[::-1]
# rev: ('blue','green','red')
colours = rev
# colours: ('blue','green','red')
```
The max() and min() functions in tuples:

```python
tuple1 = ('1','2','3')
max(tuple1)
# 3
min(tuple1)
# 1
```
The len() function returns the length of the tuple:

```python
tuple1 = ('1','2','3')
len(tuple1)
# 3
```


