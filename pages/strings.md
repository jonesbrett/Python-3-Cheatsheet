- [Return to Table of Contents](/../../)

## Strings

## String Methods

Everything in python is an object, where methods can be applied to return a manipulated version of the original object.

| Operator | Function | Source | Command | Output |
| -------- | ---- | ------- | ------- | ------- |
| .capitalize() | capitalizes a string |  text = "hello wORLD" | print(text.capitalize()) | Hello world |
| .lower() | converts all to lower case | text = "hello wORLD" | print(text.lower()) | hello world |
| .upper() | converts all to upper case | text = "hello wORLD" | print(text.upper()) | HELLO WORLD |
| .title() | converts the first letter of each word to uppercase |  text = "hello wORLD" | print(text.title()) | Hello World |
| .swapcase() | swaps the case of each letter | text = "hello wORLD" | print(text.swapcase()) | HELLO WORLD |
| .count(<sub>[,<start>[,<end>]]) | counts the number of times <sub> occurs | text = "hello wORLD" | print(text.count('o', 0, 6)) | 1 |
| .find(<sub>[,<start>[,<end>]]) | returns the index of <sub> first occurrence | text = "hello wORLD" | print(text.find('lo')) | 3 |
| .isalnum() | returns True if alphanumeric | text = "hello wORLD" | print(text.isalnum()) | False |
| .isalpha() | returns True if alphabets only | text = "hello wORLD" | print(text.isalpha()) | True |
| .isdigit() | returns True if numbers only | text = "hello wORLD" | print(text.isdigit()) | False |
| .islower() | returns True if all lowercase | text = "hello wORLD" | print(text.islower()) | False |
| .isupper() | returns True if all uppercase | text = "hello wORLD" | print(text.isupper()) | False |
| .lstrip(<sub>) | Removes leading characters <sub> argument | text = "hello wORLD" | print(text.lstrip('hel')) | lo wORLD |
| .rstrip(<sub>) | Removes trailing characters <sub> argument | text = "hello wORLD" | print(text.rstrip('RLD')) | hello wO |
| .strip(<sub>) | Removes characters <sub> argument | text = " hello wORLD " | print(text.strip()) | hello wORLD |
| .join(<sub>) | Joins characters with <sub> argument | list = ["hello", "wORLD"] | print((' ').join(list)) | hello wORLD |





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
