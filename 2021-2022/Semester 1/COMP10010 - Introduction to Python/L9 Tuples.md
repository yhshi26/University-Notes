# L9: Tuples
[COMP10010_10](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1675382/View)
###### tags: `COMP10010 - Introduction to Python`

> last lecture: indexing, index error (out of range), immutables (strings are immutable: can't change them character by character, can only reassign), constants, slicing sequences (word[x:y] extracts subsequence of sequence using specified range)

## Tuples
- similar to sequences
    - are essentially sequences looked at from a different angle
    - because of that, you can do everything with tuples that you can with sequences (and this can be done the same way)
- are immutable
    - cannot be assigned element by element

#### Example 28
``` python
# demonstrates tuples

# creates a tuple with some items and displays with for loop
tuple1 = ("item 1",
        "item 2",
        "item 3",
        "item 4",
        "item 5")
print("tuple contains:")
for item in tuple:
    print(item)
    
# get tuple length
print("tuple length:", len(tuple1))

# test for item in tuple
if "item 1" in tuple1:
    print("item 1 in tuple")
    
# display one item through an index
index = int(input("enter index for an item in tuple:"))
print("tuple[", index, "] = ", tuple1[index])

# display a slice
start = int(input("enter index for start:"))
end = int(input("enter index for end:"))
print("tuple[", start, ",", end, "] = ", tuple1[start:end])

# concatenates two tuples
tuple2 = ("item 1",
        "item 2",
        "item 3",
        "item 4",
        "item 5")
print("tuple1 + tuple 2 =", tuple1+tuple2)
```

### Creating a tuple
- assign a list of items in brackets to a variable
- list can be empty, but brackets need to be present
    - e.g. ```empty_tuple = ()```

### Tuples as conditions
- if tuple empty 
``` python
if not tuple1:
    print("tuple1 is empty")
```
- a tuple is ```true``` if it contains something
- a tuple is ```false``` if it is empty

### Printing a tuple
- can use ```print()``` or ```for```
    - ```print()``` will be preformatted

## Tuples and different types
- tuples can mix strings, integers, floats, etc.
- can have tuples within tuples

#### Example 29
``` python
# demonstrates mixed tuples

tuple1 = ("string", 1, 3.14)
print(tuple1)

print("tuple1 displayed element by element:")
for element in tuple1:
    print(element)
```

### len(), slicing
- can use ```len()``` on tuples
    - returns number of elements in tuple
```print(len(tuple1))```
- can slice tuples like sequences
```print(tuple1[start:finish])```

### in and tuples
- can use ```in``` operator on tuples like sequences
- ```something in tuple1``` returns ```true``` if ```something``` is an element of the tuple ```tuple1```, ```false``` otherwise

> reminder: ```in``` looks small and harmless, but is a powerful operator

### Immutability and mutability
- while tuples are immutable, you can change them fairly easily
    - be aware this involves creating/assigning new tuples all the time
- this takes tuple ```tuple1``` and creates a *new tuple* that is concatenated to ```tuple2``` and assigns it to ```tuple1```
``` python
tuple1 += tuple2
```
