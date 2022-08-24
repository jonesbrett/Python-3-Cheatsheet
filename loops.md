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
## The else Statement

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
