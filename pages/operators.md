- [Return to Table of Contents](/../../)  

## Basic Operators

The following operators are considered as basic operators:

| Operator | Function | Example |
| -------- | ---- | ------- |
| input() | Prompts the user to enter a value | input('What is your name: ?') |
| print() | Prints to the console | Hello World |
| int() | Specifies the value is a integer | age = int(38) |
| float() | Specifies the value is float | age = float(38.5) |
| str() | Specifies that the value is a string | name = str(Brett) |
| len() | Specifies the length of a object | len(Brett) is 5 |

## Print Operators

The print operator has three additional operators:

| Operator | Function | Example | Ouput |
| -------- | ---- | ------- | ----- |
| end= | Denotes what to place at the end of the print statement | print('Hello World', end='!') | Hello World! |
| sep= | Denote what use a separating index | print('Hello', 'World', sep='#') | Hello#World |
| + | Concatenates two string together | print('Hello' + 'World') | HelloWorld |

## Unary Operators

Unary operators have a + or - sign infornt of the value:

-2
+5


## Arithmetic Operators - (Binary Operators)

Arithmetic operators are used with numeric values to perform common mathematical operators:

| Operator | Name | Example | Order of Operators | Output |
| -------- | ---- | ------- | ------------------ | ------ |
| ** | Exponentiation | x ** y | 1st | These are calculated from right to left: 2 ** 2 ** 3 = 2 ** (2 ** 3) | 
| // | Floor division | x // y | 1nd | If both operands are an integer the floor division operator will return an integer |
| * | Multiplication | x * Y | 2nd |
| / | Division | X / y | 2nd | Returns a float |
| % | Modulus | x % y | 2nd | Returns an Integer |
| + | Addition | x + Y | 3rd |
| - | Subtraction | x - y | 3rd |


## Assignment Operators

Assignment operators are used to assign values to varialbes:

| Operator | Example | Same As |
| -------- | ------- | ------- |
| = | x = 5 | x = 5 |
| += | x += 3 | x = x + 3 |
| -= | x -= 3 | x = x - 3 |
| *= | x *= 3 | x = x * 3 |
| /= | x /= 3 | x = x / 3 |
| %= | x %= 3 | x = x % 3 |
| //= | x //= 3 | x = x // 3 |
| **= | x **= 3 | x = x ** 3 |
| &= | x &= 3 | x = x & 3 |
| \|= | x \| = 3 | x = x \| 3 |
| ^= | x ^= 3 | x = x ^ 3 |
| >>= | x >>= 3 | x = x >> 3 |
| \<<= | x \<< = 3 | x = x \<< 3 |


## Comparison Operators

Comparison operators are used to compare two values:

| Operator | Name | Example |
| -------- | ---- | ------- |
| == | Equal to | x == y |
| != | Not equal to | x != y |
| > | Greater than | x > y |
| \< | Less than | x \< y |
| >= | Greater than or equal to | x >= y |
| \<= | Less than or equal to | x \<= y |


## Logical Operators

Logical operators are used to combine conditional statements:

| Operator | Description | Example |
| -------- | ------------| ------- |
| and | Returns True if both statements are true | x \< 5 and x \< 10 |
| or | Returns True if one of the statements is true | x \< 5 or x \< 4 |
| not | Reverse the result, returns False if the result is true | not(x \< 5 and x \< 10) |


## Identity Operators

Identity operators are used to compare the objects, not if they equal, but if they are actually the same object,
with the same memory location:

| Operator | Description | Example |
| -------- | ------------| ------- |
| is | Returns True if both variables are the same object | x is y |
| is not | Returns True if bot varilables are not the same object | x is not y |


## Membership Operators

Membership operators are used to test if a sequence is presented in an object:

| Operator | Description | Example |
| -------- | ------------| ------- |
| in | Returns True if a sequence with the specified value is present in the object | x in y |
| not in | Returns True if a sequence with a specified value is not present in the object | x not in y |


## Bitwise Operators

Bitwise operators are used to compare (binary) numbers:

| Operator | Name | Description |
| -------- | ---- | ----------- |
| & | AND | Sets each bit to 1 if both bits are 1 |
| \| | OR | Sets each bit to 1 if one of two bits are 1 |
| ^ | XOR | Sets each bit to 1 if only one of two bits is 1 |
| ~ | NOT | Inverts all the bits |
| \<< | Zero fill left shift | Shift left by pushing zeros in the the right and let the leftmost bits fall off |
| >> | Signed right shift | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off |




- [Return to Table of Contents](/../../)  
