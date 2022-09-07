- [Return to Table of Contents](/../../)

## Comments

Comments are used to explain the code and to make it more readable:

```python
# This is a print statement which will diaplay, Hello World!
print('Hello World!')

Hello World!
```

Comments can be place above code or next to code:

```python
print('Hello World!') #This is a print statement which will diaplay, Hello World!

Hello World!
```

Comments can also be used to ingore lines of code:

```python
# This is a print statement which will diaplay, Hello World!
#print('Hello World!')
print('Good Morning World!')

Good Morning World!
```

## Numerical Representations

Number can use underscores to make them more readable:

```python
num = 12000300
print(num)

12000300

num = 12_000_300
print(num)

12000300
```

## Scientific Notation

Scientific Numbers use an "e" or "E" to indicate to the power of 10:

3e4 = 3E4 = 3 * 10000 = 30000
3e-4 = 3E-4 = 3 * 1/10000 = 0.0003

Python always uses Scientific Numbers for large numbers:

```python
print(0.000000000000000000000000005)

5e-27
```

## Accuracy of Floating-point Numbers

Float numbers are not 100% accurate:

```python
print(0.1 + 0.1 + 0.1)

0.30000000000000004
```

## Octal Numbers

Octal Numbers start with 0O or 0o:

```python
print(0o123)

83
```

## Hexadecimal Numbers

Hexadecimal Numbers start with 0X or 0x:

```python
print(0x123)

291
```
## String Formmatting

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
print =("hokus", "pokus", sep='!')

hokus!pokus

#Note there is no exclamation after 'pokus'
```










- [Return to Table of Contents](/../../)
