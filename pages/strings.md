- [Return to Table of Contents](/../../)

## Strings

## String Methods

Everything in python is an object, where methods can be applied to return a manipulated version of the original object.

| Operator | Function | Source | Command | Output |
| -------- | ---- | ------- | -------- | ------- |
| .capitalize() | capitalizes a string |  text = "hello wORLD" | print(text.capitalize()) | Hello world |
| .lower() | converts all to lower case | text = "hello wORLD" | print(text.lower()) | hello world |
| .upper() | converts all to upper case | text = "hello wORLD" | print(text.upper()) | HELLO WORLD |
| .title() | converts the first letter of each word to uppercase |  text = "hello wORLD" | print(text.title()) | Hello World |
| .swapcase() | swaps the case of each letter | text = "hello wORLD" | print(text.swapcase()) | HELLO WORLD |
| .count() | counts the number of times (argument) occurs | text = "hello wORLD" | print(text.count('o', 0, 6)) | 1 |
| .find() | returns the index first occurrence  of argument| text = "hello wORLD" | print(text.find('lo')) | 3 |
| .isalnum() | returns True if string is alphanumeric | text = "hello wORLD" | print(text.isalnum()) | False |
| .isalpha() | returns True if string is alphabets only | text = "hello wORLD" | print(text.isalpha()) | True |
| .isdigit() | returns True if string is numbers only | text = "hello wORLD" | print(text.isdigit()) | False |
| .islower() | returns True if string is all lowercase | text = "hello wORLD" | print(text.islower()) | False |
| .isupper() | returns True if string is all uppercase | text = "hello wORLD" | print(text.isupper()) | False |
| .lstrip() | Removes leading characters in (argument) | text = "hello wORLD" | print(text.lstrip('hel')) | lo wORLD |
| .rstrip() | Removes trailing characters in (argument) | text = "hello wORLD" | print(text.rstrip('RLD')) | hello wO |
| .strip() | Removes characters in (argument) | text = " hello wORLD " | print(text.strip()) | hello wORLD |
| .join() | Joins characters in  (argument) | list = ["hello", "wORLD"] | print((' ').join(list)) | hello wORLD |





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
