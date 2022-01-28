# L10: Functions
[COMP10010_11](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1682024/View)
###### tags: `COMP10010 - Introduction to Python`

> last lect: creating tuples (sequences in brackets assigned to a variable), tuples as conditions (tuple false if empty, true otherwise), printing a tuple directly using print or using a for loop, using len() and slicing tuples, immutability and mutability 

## Functions
- py has built-in functions we've looked at such as ```len()```, ```range()```, etc.
- you can make your own functions as well

### Divide and conquer
- creating well defined functions allows you to break your code into manageable bits
- well defined means it performs a clear, independent task, e.g. print a table, compute overall tax, load file, etc.
- once you have written and tested a function, and know it works, you can forget about that bit of code/task

### Readability
- by virtue of writing functions, your main code becomes shorter and easier to read
    - instead of a long program (potentially [spaghetti code](https://en.wikipedia.org/wiki/Spaghetti_code)), you will have a few bits, each one of which is essentially independent of others and can be read/tested separately
- if the asks put into functions are repetititve, overall code will be considerably shorter
    - don't need to repeat code lengthening program (with risk of introducing errors, etc.)
    - e.g. using sqrt(x) instead of writing 5 lines of code every time you want to calculate a square root 

### Reusing functions
- once you have been programming for a while, you'll find you have written functions for many typical tasks
- gradually, these may build up into libraries and allow you to create complex programs very fast, as much of the code is already there

## Creating a function
``` python
def functionName():
    """optional comment"""
    block of code
```

### Parameters and return values
- functions sometimes need something to work on, this is typically some argument given to the function as a parameter (in its own brackets)
    - note: the moment a function reaches a return statement, it leaves the function (does not execute code after, jumps out of function)
- functions sometimes need to return something to the main program

#### Example 36
``` python
# volumes and boxes

def boxVol(length,width,height):
    return length*width*height

print("computing volume of box")
l = int(input("length: "))
w = int(input("width: "))
h = int(input("height: "))

print("box volume: ", boxVol(l,w,h))
input("enter to exit")
```

#### Example 37
``` python
# receive and return

def give_five():
    five = 5
    return five

def ask_yes_no(question):
    """ask a yes or no question"""
    response = None
    while response not in ("y", "n"):
        response = input(question).lower()
    return response

# main
print("message: ")

number = give_five()
print("from give_five(): ", number)

answer = ask_yes_no("enter 'y' or 'n': ")
print("response: ", answer)

input("enter to exit")
```

### Example 38
``` python
import math

def sum_sqrt(N):
    tot = 0
    for i in range(1,N+1):
        tot += math.sqrt(i)
    return tot

# main
q = int(input("number: "))
print("sum of square roots of integers up to q: ", sum_sqrt(q))

input("enter to exit")
```

