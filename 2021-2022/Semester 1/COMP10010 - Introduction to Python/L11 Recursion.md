# L11: Recursion
[COMP10010_12](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1685576/View)
###### tags: `COMP10010 - Introduction to Python`

> last lect: functions, creating functions (def functionName():), parameters, return values

## Recursive functions
- functions that call themselves
- works well with some problems
    - e.g. fibonacci sequence:
    - f(0) = 0, f(1) = 1, f(n) = f(n-1), f(n-2)

#### Example 38x
``` python
def fibonacci(N):
    if N<=0:
        return 0
    elif N==1:
        return 1
    else:
        return fibonacci(N-1) + fibonacci(N-2)
```

#### Example 30x (1)
``` python
import random

N = int(input("number random numbers: "))

seq_num = ()
for i in range(0,N):
    temp = random.randrange(0,100),
    seq_num += temp

print("random sequence: ", seq_num)

sorted_seq_num = ()
```

## Sorting
- each time we pick a max and add it to the sorted tuple
- each time the starting tuple is shortened by 1
    - we need to do this ```len(tuple)``` times with a ```for``` loop
- notice that while we spot a max by just looking at a (short) list, a computer would need to iterate through all the elements (another ```for``` loop nested in the one above)

#### Example 30x (2)
``` python
for i in range(0,N):
    maxv = 0
    maxp = -1
    for j in range(0,len(seq_num)):
        if seq_num[j]>maxv:
            maxv = seq_num[j]
            maxp = j
    sorted_seq_num += seq_num[maxp],
    seq_num = seq_num[0:maxp]+seq_num[maxp+1]

print("sorted: ", sorted_seq_num)
```

## Lists
- tuples are good for organising different types o fvariables
- immutability, however, can be a limitation
- while there are ways around it, maintaining a large tuple and having to copy it every time an element is added to it puts a strain on the computer
- lists are a great way around this, in that they behave like tuples but are mutable

#### Example 31
``` python
# hero's inventory 3.0
# demonstrates lists

inventory = ["sword", "armor", "shield", "healing potion"]
print("items:")
for item in inventory:
    print(item)

input("press enter to continue")

# get length of list
print("length:", len(inventory))

input("press enter to continue")

# test for membership in
if "healing potion" in inventory
    print("you will live to fight another day")

# display one item through an index
index = int(input("enter index number for item in inventory: "))
print("at index," index, "is", inventory[index])

# display slice
start = int(input("enter start index: "))
end = int(input("enter end index: "))
print("inventory[", start, ":", end, "]:", end=" ")
print(inventory[start:end])

# concatenate two lists
chest = ["gold", "gems"]
print("you find a chest which contains: ")
print(chest)
print("you add the contents of the chest to your inventory")
inventory += chest
print("new inventory:")
print(inventory)

input("press enter to continue")

# assign by index
print("you trade your sword for a crossbow")
inventory[0] = "crossbow"
print("new inventory:")
print(inventory)
input("press enter to continue")

# assign by slice
print("you use your gold and gems to buy an orb of future telling")
inventory[4:6] = ["orb of future telling"]
print("new inventory:")
print(inventory)
input ("press enter to continue")

# delete element
print("in a great battle, your shield is destroyed")
del inventory[2]
print("new inventory:")
print(inventory)
input("press enter to continue")

# delete a slice
print("your crossbow and armor are stolen by thieves")
del inventory[:2]
print("new inventory")
print(inventory)
input("press enter to exit")
```

### Lists functionality
- pretty much everything that can be done with tuples:
    - ```len()```
    - using ```in```
    - indexing
    - slicing
    - concatenating
- additional things that can't be done with tuples:
    - assinging a new element by index
    - assigning a new slice
    - deleting an element
    - deleting a slice
    - and dedicated methods...


