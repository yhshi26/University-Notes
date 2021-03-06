# L3: Manipulating data 
[COMP10010_04](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1641679/View)
###### tags: `COMP10010 - Introduction to Python`
> previous lecture content: arithmetic, operators, shortcuts, variables
> extended on: print(), input()

## Manipulating strings
Py provides many functions that allow the manipulation of strings stored within variables, substitute parts of them, turn lowercase to uppercase and vice versa, etc.

### Example 1
``` python
# take user input as quote
# modify to uppercase, lowercase, and title versions of user input
quote = input("input quote:")
print(quote)
print("uppercase:", quote.upper())
print("lowercase:", quote.lower())
print("as title:", quote.title())
```

### Example 2
``` python
# modify segment of string
quote = "x"
print(quote)
print("replace segment", quote.replace("x","y"))
print("quote is unchanged:", quote)
```

## Logic error with input()
input() only returns strings:
- this is benificial as it ensures nothing typed by the user will cause a compile-time error (e.g. inputting wrong type, because anything can be made a string)
``` python
# demonstrates logic error with variables
print("add 2 numbers")
n1 = input("number 1:")
n2 = input("number 2:")
print("sum of", n1, "and", n2, "is:", n1+n2)
```
- this may look harmless, but compiling results with a logic error where n1 and n2 are treated as strings instead of numbers
- because of that, the printed sum is not necessarily what we expect

### Turning a string into a number
``` python
# demonstrates changing types
print("add 2 numbers")
n1 = int(input("number 1:"))
n2 = int(input("number 2:"))
print("sum of", n1, "and", n2, "is:", n1+n2)
```

#### int() compile errors
- int() can only change types of what look like numbers
``` python
ValueError: invalid literal for int() with base 10:
'[the argument, if it does not look like a number]'
```

#### int() on floating point 
``` python
>>> a=int(1.4)
>>> print(a)
1
>>> a=int(1.8)
>>> print(a)
1
>>> a=int(-3.9)
>>> print(a)
-3
```

## Type conversion functions
- float(): converts argument to floating point
- int(): converts argument to integer
- str(): converts argument to string

These are explicit conversions. Notice that py implicitly does some conversions  for you. 
- e.g. when you divide integers, py runs the computations as float

## Composing functions
- can condense lines of code with functions
### Example 1
``` python
# the following code can be shortened
n1 = input("number 1:")
n1_int = int(n1)
# shortened code
n1_int = int(input("number 1:"))
```
### Example 2
``` python
# demonstrates how all arguments in print are computed before printing
print("*5 =", 5*int(input("number:")))
```
