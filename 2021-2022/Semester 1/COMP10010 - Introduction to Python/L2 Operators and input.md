# L2: Operators and input
[COMP10010_03](https://https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1636741/View)
###### tags: `COMP10010 - Introduction to Python`
> previous lecture content: comments (# in py), input() and print() functions

## Expressions with numbers
- expressions with numbers are evaluated
- on compiling, once computations complete, the expression is substituted with its result
> note: expressions are only computed when numbers and symbols are not in quotes (otherwise they will be treated as characters and strings)

### Example
```
>>> print(5+5)
10
>>> print("5"+"5")
55
>>> print("5+5")
5+5
```

### Operators
|          |operation  |
| -------- | -------- |
|+ | addition|
|- |subtraction|
|* |multiplication|
|/ |division|
|// |integer division|
|% |modulus/mod (remainder of integer division)|

``` python
>>> print(107//4)
26
>>> print(107%4)
3
```

### Integers vs. floating point
``` python
>>> print(16*3)
48
>>> print(103/3)
34.333333333333336
```
- line 1's expression computed an integer
- line 2's expression computed a floating point
- computers store each data type differently

## Variables
- is a storage place for information (py reserves memory for variables, then stores values in the reserved memory locations)
- is called a variable as the stored information can change throughout compiling

### Example
``` python
# this program says hi to a person
# demonstrates the use of a variable
name = "n"
print("hi", name)
input("press enter to exit program")
```
- line 1 creates a string variable containing the character n
- the name variable can store other things to (its assignment can change through assigning another value)

### Nomenclature
#### Syntax
- variable names can only contain letters, numbers and underscores "_"
- a variable name cannot start with a number 
#### Etc.
- ensure name is descriptive
- concise (easier to type, less risk of mistyping and causing an error)

## Shortcuts

|statement |shortcut  |
| -------- | -------- |
|c = c + i |c+=i      |
|c = c - i|c-=i|
|c = c * i|c*=i|
|c = c / i|c/=i|

## User input
### [input([prompt])](https://docs.python.org/3/library/functions.html#input) function
- if the prompt argument is present, it is written to standard output without a trailing newline
- the function then reads a line from input, converts it to a string (stripping a trailing newline), and returns that 
    - this returned string can be stored in a variable
    ``` python
        input_string = input("")
    ```

### Example
``` python
# intakes user input
# prints user input
user_input = input("provide input")
print(user_input)
input("\npress enter to exit")
```
