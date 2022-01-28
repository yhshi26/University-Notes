# L4: Modules
[COMP10010_05](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1649450/View)
###### tags: `COMP10010 - Introduction to Python`

> content covered last lect: string functions (upper, lower, title, replace), variable types (string, int, floating point), type conversion functions (str(), int(), float()), composing functions

## Importing modules
- many functions in py are not part of the main package, they are in modules
    - some come with py, and many others may be developed by others and distributed
    - you can even make your own
- to tell the py compiler you want to use a function from module X, you need to write:
``` python
import X
```

## The random module
### Random numbers
``` python
# simulate a die using random numbers
import random

die1 = random.randint(1,6)
print(die1)
```
- to create random numbers we have used the random module
- within that module there is a randint() function that takes two values as arguments, e.g.:
``` python
# this generates a random integer between 15 and 100 (included)
random.randint(15,100)
```
- within random there is also a randrange()function
- if you give it one value, it generates random numbers between 0 (included) and that value (excluded), e.g.:
``` python
# this generates a random integer between 0 and 99 (included)
random.randrange(100)
```

## Control
> in order to make useful programs we need something more than a list of statements - we cannot even count up to an arbitrary number if our program is a fixed list of statements
- we need to control the flow of statements
    - we can do this by making some statements conditional on what is going on (e.g. the state of some variables)

### If statements
``` python
# if the condition is met, the statement is executed; 
# the condition is something that has to be true or false
if condition: 
    statement
```

#### Example 11
``` python
# password
# demonstrates the if statement
print("Welcome to System Security Inc.")
print("--where security is our middle name\n")
password = input("Enter your password: ")
if password == "secret":
    print("Access Granted")
input("\n\nPress the enter key to exit."
```

#### Conditions
- aything that can be interpreted as true or false is a condition
- in example 11, the condition was:
    - password == "secret"
    - notice the == (comparatively, a single = would be assignment)

    #### Relational operators
    < less than
    <= less than or equal to
    \> greater than
    \>= greater than or equal to
    == equal to
    != not equal to
  
### Else statements
``` python 
# sometimes you want to make a choice between two options depending on a condition
if condition:
    do something
else:
    do something else
```

### Else if statements
``` python
# sometimes the choice is one out of many
if condition:
    do thing 1
elif condition2:
    do thing 2
...
else
    do thing N
```

## Indentations and blocks
> the statement controlled by the if condition in example 11 was indented to the right
- indentation is **mandatory** in py
- you can create a *block* by indenting multiple lines by the same amount
    - a block behaves like a single statement
    - for instance, an ```if``` will control the whole block rather than only the first statement following it

### How much indentation?
- make your choice and stick to it
- tabs or spaces are OK, just don't mix them (you can't really tell which is which by just looking at it)
    - 2-4 spaces is OK
    - 1 tab is OK
    - just be consistent..
- when writing code within IDLE, let IDLE decide

### Note on Py vs. other languages
- in py indentation has a precise meaning, and presence or absence of it results in different behaviours
- in many other languages indentation has no meaning other than as a visual aid
    - that is: indentation is for you (so it's optional); the block is marked in other ways
    - for instance in C/C++ it's enclosed between curly braces {}
    - if you switch to other languages in another life, be aware of this..

