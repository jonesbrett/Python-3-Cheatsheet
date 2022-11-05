- [Return to Table of Contents](/../../)

## Strings

### Concatenating

Concatenating two strings with the + sign:

```python
text = 'hokus' + 'pokus'
print(text)

hokuspokus
```

Multipling strings with the * sign:

```python
print('hokus' * 5)

hokushokushokushokushokus
```

### The End Keyword

The 'end' keyword can be used to aviod a new line and specify the end of a string with a defined attribute.

```python
text = ["hokus", "pokus"]
for words in text:
    print(words, end="!")

hokus!pokus!
```

### The Sep Keyword

The 'sep' keyword can be used to specify the seperator of a string with a defined attribute.

```python
print("hokus", "pokus", sep='!')

hokus!pokus

#Note there is no exclamation after 'pokus'
```

### Splitting Strings

We can split string using the '.split(delimiter)' argument, if we don't specify the argument it
defaults to spaces.

string_name.split(delimiter)

```python
man_its_a_hot_one = "Like seven inches from the midday sun"
print(man_its_a_hot_one.split())

['Like', 'seven', 'inches', 'from', 'the', 'midday', 'sun']
```

### Joining Strings

You can join string using the '.join()' method, the argument now refers to the list and the delimiter
is at the beginning.

'delimiter'.join(list_you_want_to_join)

```python
my_munequita = ['My', 'Spanish', 'Harlem', 'Mona', 'Lisa']
print(' '.join(my_munequita))
'My Spanish Harlem Mona Lisa'
```

### Format Function

You can use the '.format()' function to insert values from different lists using keys.

```python
colors = ['red', 'yellow', 'green', 'white', 'black', 'blue', 'purple']
count = ['24', '34', '30', '28', '26', '22', '17']
for color in colors:
  print(
    'We sold {0} of {1} threads today.'
    .format(count, color)
    )
```





- [Return to Table of Contents](/../../)
