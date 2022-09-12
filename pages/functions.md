## Functions

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

# Note, you can over write the global variable from with in the function using the 'global' command:

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
```
