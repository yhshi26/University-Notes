# L15: Variable and function scopes
[COMP10010_16](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1707009/View)
###### tags: `COMP10010 - Introduction to Python`

> last lect: writing onto files

## Scope
- let's define scope more precisely
- it goes hand in hand with encapsulation, and is essential to functions (and more)

### Sealing off functions
- it is essential that functions are sealed off from the rest of the code
- that is, you want functions ot have a hard time modifying sutff in the mian code, other than through their controlled access points (parameters and return values)
- the main element of this is that variables inside fucniton are only alive for as long as the function is: their scope is the function itself

### It doesn't stop there
- more in general, a variable is alive only for the duration of the block in which it has been created
- create a variable (name it the first time) within the block controlled by a for loop, for instance, and it will die once you are out of the loop (the block is its scope)
- we say that all these variables are local to the block/function

## Global variables
- you can also have variables that live throughout a program; generally these will be defined in the main program
- these variables are global
- while there are advantages to them (you don't need to explicitly pass them around through arguments and return values), you have to use them very carefully

### Accessing global variables
- you can read a global variable from anywhere in your program, including from within a function
- in order to change a global variable within the local scope of a funciton though, you need to declare it as global (to state it is not a new, local version of it)

### Shadowing
- if, when in a local scope, you declare a variable (by assigning something to it) of the same name as a global one, and you have ne=ot declared it as global, you are creating a new local variable
- that variable will shadow th eglobal one for as long as it is around (its scope)
- you have no way to access the global variable, including for reading, for as long as the shadowing local one is alive

#### Example 42
``` python
# global reach
# demonstrates global variables

def read_global():
    print("from inside the local scope of read_global(), value is:", value)

def shadow_global():
    value = -10
    print("from inside the local scope of shadow_global(), value is:", value)
    
def change_global():
    global value
    value = -10
    print("from inside the local scope of change_global(), value is:", value)
    
# main
# value is a global variable because we're in the global scope here
value = 10
print("in the global scope, value has been set to:", value, "\n")

read_global()
print("back in the global scope, value is still:", value, "\n")

shadow_global()
print("back in the global scope, value is still:", value, "\n")

change_global()
print("back in the global scope, value is still:", value, "\n")

input("\npress enter to exit")
```
## When to use global variables
- try not to 
- in general, they create confusion, especially if you modify them
- bouncing back and forth between main code and functions to figure out where something has gone wrong is bad
- use ```global``` sparingly or not at all
- global constants (which in py are variables) are ok

### Shared references
- there is a subtle issue with lists: what you are keeping in the variable is an address, rather than the object itself
- so if you assign that variable ot another variable, you will be copying the address, not the whole object
- the main consequence of this is that if you change the list, it wil change for all versions of it as they aren't actual copies



