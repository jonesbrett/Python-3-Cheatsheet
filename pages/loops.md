- [Return to Table of Contents](/../../)

## The While Loop

With the 'while' loop we can execute a set of statements as long as a condition is true:

```python
i = 1
while i < 6:
    print(i)
    i += 1

# 1
# 2
# 3
# 4
# 5
```

## The Break Statement

With the 'break' statement we can stop the loop even if the 'while' condition is true:

```python
# Exit the loop when i is 3
i = 1 
while i < 6:
    print(i)
    if i == 3:
        break
    i += 1

# 1
# 2
# 3
```

## The Continue Statement

With the 'continue' stateement we can stop the current iteration, and contine with the next:

```python
# Continue to the next iteration if i is 3:
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)

  # 1
  # 2   # Note that 3 is missing
  # 4
  # 5
  # 6
```
## The Else Statement

With the 'else' statement we can run a block of code once then the condition no longer is true:

```python
# Print a message once the condition is false:
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")

# 1
# 2
# 3
# 4
# 5
# i is no longer less than 6
```

## The For Loop

A 'for' loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a sting):

```python
# Print each fruit in a fruit list:
fruits = ['apple', 'banana', 'cheery']
for x in fruits:
  print(x)

apple
banana
cherry
```

## Looping Through a String

Even strings are iterable objects, they contain a sequence of characters:

```python
# Loop through the letters in the word "banana":
for x in "banana":
  print(x)

b
a
n
a
n
a
```

## The Break Statement

With the 'break' statement we can stop the loop before it has looed through all the items:

```python
# Exit the loop when x is "banana":

fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
  if x == "banana":
    break

apple
banana 

# Exit the loop when x is "banana", but this time the break comes before the print:

fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    break
  print(x)

apple
```

## The Continue Statement

With the 'continue' statement we can stop the current iteration of the loop, and continue with the next:

```python
#Do not print banana:

fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    continue
  print(x)

apple
cherry 
```

## The range() Function

To loop through a set of code a specified number of time, we can use the range() function, the range() function retunrs a sequence of numbers, starting from 0 (by defaul)t, and increments by 1 (by default), and ends at a specified number:

``` python
# Using the range() function:

for x in range(6):
  print(x)

0
1
2
3
4
5 

# Note that range(6) is not the values of 0 to 6, but the values 0 to 5.
# The range() function defaults to 0 as a starting value, however it is possible to specify the starting value by adding a parameter: range(2, 6), which means values from 2 to 6 (but not including 6):

for x in range(2, 6):
  print(x)

2
3
4
5

# The range() function defaults to increment the sequence by 1, however it is possible to specify the increment value by adding a third parameter: range(2, 30, 3):

#Increment the sequence with 3 (default is 1):
for x in range(2, 30, 3):
  print(x)

2
5
8
11
14
17
20
23
26
29 
```

## The Else in For Loops

The 'else' keyword in a 'for' loop specifies a block of code to be exercuted when the loop is finished:

```python
#for x in range(6):
  print(x)
else:
  print("Finally finished!")  

0
1
2
3
4
5
Finally finished!

# Note: The else block will NOT be executed if the loop is stopped by a break statement.

# Break the loop when x is 3, and see what happens with the else block:

for x in range(6):
  if x == 3: break
  print(x)
else:
  print("Finally finished!") 
0
1
2 
```

## Nested Loops

A nested loop is a loop inside a loop. The 'inner loop' will be executed one time for each iteration of the 'outer loop':

```python
#Print each adjective for every fruit:
 adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
  for y in fruits:
    print(x, y)

red apple
red banana
red cherry
big apple
big banana
big cherry
tasty apple
tasty banana
tasty cherry 
```

## The Pass Statement

'for' loops cannot be empty, but if you for some reason have a 'for' loop with no content, then put the 'pass' statement to aviod getting an error:

```python
for x in [0, 1, 2]:
  pass

```


