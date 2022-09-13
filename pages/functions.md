- [Return to Table of Contents](/../../)  

### The Print Function

Print is a built in function which displays output to the terminal:

```python
print('Hello World!')

Hello World!
```
Print has two optional parameters, 'sep' and 'end'. The 'sep' for separator, specify how to 
separator the objects, the end for end specifies what to print at the end (the default is a new line(\n)):

```python
print("1", "2", "3", "4", "5", sep="-")

1-2-3-4-5

print("1", "2", "3", "4", "5", end="-")

1 2 3 4 5-
```

### The Length Function

The Length function gives you the number of elements in a collection:

```python
print(len('Hello World!'))

12
```

### The Input Function

The Input prompts for user input:

```python
number = input('What is the number?: ')
print(number)

What is the number?: 25
25
```

### Defining your own Function

You can define your own Functions using 'def' for definision:

```python

def greet():
    print('Hello, my dear!')

greet()

Hello, my dear!
```

Assigning arguments to functions is done after calling the function:

```python
def print_letter_count(text, letter):
    counter = 0
    for char in text:
        if char == letter:
            counter += 1
    print('Number of', letter, 'is', counter)

print_letter_count('welcome', 'e')

Number of e is 2

# Note, you can not switch the arguments around unless you use the key words:

print_letter_count(letter='e', text='welcome')

Number of e is 2
```
### Veriables and Functions

There are two types of veriables, those being 'Global' and 'Local'. The veriable definined in 
a function is called a 'Local' and is only available to that function. 'Global' veriables are 
avialable inside and outside of functions:

```python
def show_truth():
    mysterious_var = 'New Surprise!'
    print(mysterious_var)

mysterious_var = 'Surprise!'
print(mysterious_var)
show_truth()
print(mysterious_var)

Suprise!
New Suprise!
Surprise!

# Note, you can over write the global variable from within the function using the 'global' command:

def show_truth():
    global mysterious_var
    mysterious_var = 'New Surprise!'
    print(mysterious_var)

mysterious_var = 'Surprise!'
print(mysterious_var)
show_truth()
print(mysterious_var)

Suprise!
New Suprise!
New Suprise!

# Note, you can also '.append' to 'Global' veriables within the function, (List and Dictionaries only):

def show_truth():
    mysterious_var.append("New Surprise!")
    print(mysterious_var)


mysterious_var = ["Surprise!"]
print(mysterious_var)
show_truth()
print(mysterious_var)

['Surprise!']
['Surprise!', 'New Surprise!']
['Surprise!', 'New Surprise!']
```
- [Return to Table of Contents](/../../)  
