# L7: Loops, sequences, tuples
[COMP10010_08](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1665015/View)
###### tags: `COMP10010 - Introduction to Python`

> last lect: how to plan a program
> 
> learning objectives: ```for``` loops, strings as sequences, tuples (like many variables at once), manipulating sequences

## For loops
- a string is a sequence of letters
- ```for``` iterates through sequences, beginning to end
    
``` python
for letter in word:
    print(letter)
```

#### Example 22
``` python
# demonstrates for loop with string

word = input("input word:")

print("each letter in the word:")
for letter in word:
    print(letter)
```

#### Analysis of the loop
- ```letter``` is created at the beginning of the for loop
- for each letter in word, from first to last
    - it is copied into ```letter```
    - the statement or block within the for is executed

### Counting with ```for```
``` python
# range() creates a sequence of numbers
# between 0 and 1 less than its argument (inclusive)

seq_num = range(100)

for i in seq_num:
    print(i,end" ")
```

#### More about ```range()```
- can be used with more than 1 argument

``` python
seq_num = range(-10,100,5)

for i in seq_num:
    print(i,end=" ")
```

- ```range(x)```: sequence between ```0``` and ```x-1``` (inclusive)
- ```range(x,y)```: sequence between ```x``` and ```y-1``` (inclusive)
- ```range(x,y,z)```: sequence between ```x``` and ```y-1``` (inclusive) in steps of ```z```

#### Example 23
``` python
# sum of cubes

max_int = int(input("input number:"))

tot = 0
for i in range(1,max_int+1):
    tot += i*i*i

print("the sume of cubed integers up to", max_int, "is", tot)
```

### Manipulating strings
- strings are sequences
- plenty of functions in py to manipulate sequences, finding characters or substrings, measuring lengths, etc.
    - incidentally, we have already seen some string functions, like ```str.upper()```, ```str.lower()```, ```str.title()```, though those were exclusive to strings, not valid for all sequences

#### Example 24
``` python
# message analyser
# demonstrates the len() function and the in operator

message = input("enter a message:")

print("the length of the message:", len(message))
print("most common letter in english langauge, 'e'")
if "e" in message:
    print("is in the message")
else:
    print("is not in the message")
```

#### Analysis 
- ```len(message)```:  ```len()``` takes a sequence (not necessarily a string) as input, counts its elements and returns the count (as an int)
- ```if "e" in message:```
    - the interesting bit here is ```in```
    - ```sequence1 in sequence2``` is true if ``` sequence1``` is present within ```sequence2```
    
#### Note on ```in```
- can do different things
- ```for x in sequence```
    - scans all of ```sequence``` putting its elements, 1 by 1, into ```x```
- ```if something in sequence```
    - checks if ```something``` is in ```sequence```

### Sequential access
- with the ```for``` loop we are able to access a sequence in sequential order
- that is, we start from the beginning and go through the sequence one element at a time
- this is not ideal if you want to access an element in the middle (or at the end) of the sequence, as you would have to go through all the other elements before it

#### Random access: indexing
- in py, you can access any element of a sequence at once through indexing
- essentially you pick an element by its position (index)
- there are a 2 quirks to this:
    - element positions start at 0, that is, the first element on the list has index 0
        - the last element in a sequence of length N is at index N-1
    - a negative index reads a sequence from its end
        - -1 is the last element, -2 the second last, etc.

#### Example 25
``` python
# random access
# demonstrates string indexing

import random

word = "index"
print("the word is: ", word, "\n")

high = len(word)
low = -len(word)

for i in range(10):
    position = random.randrange(low, high)
    print("word[", position, "]\t", word[position])

input("enter to exit")
```


