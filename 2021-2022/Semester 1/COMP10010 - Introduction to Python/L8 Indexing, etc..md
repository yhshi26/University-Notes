# L8: Indexing, etc.
[COMP10010_09](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1673830/View)
###### tags: `COMP10010 - Introduction to Python`

> assignment 3: 1. user input number N, 2. all prime numbers between 1 and N inclusive print to screen, 3. sum of squares of all prime numbers between 1 and N inclusive computed and print to screen, 4. user asked if they want to compute new sum of squared numbers, if yes, repeat
> 
> worth 20% of final mark

> last lect: ```for``` loops, ```while``` loops, ```range()``` (can have up to 3 arguments - range determining arguments, and step), ```len(string)``` (length function), the ```in``` particle, indexing (accessing elements in sequences)

#### Example 25: wrong index
``` python
# demonstrates what happens if you use the wrong index

word = input("word:")
endw = len(word)

i = 0
while i<=endw:
    print(i,end=" ")
    print(word[i])
    i+=1
```

- incurs index error: string index out of range
- fix: ```while i<endw:``` or ```while i<=endw-1:```

### Strings are immutable
- cannot change them character by character by indexing
    - can be reassigned
    - cannot do something like: ```string[n] = "c"```

#### Example 26
``` python
# trying to change immutables

name = "yosra"
print(name)

name = "hashim"
print(name)

name[1] = "a"
print(name) # code won't reach this line, crashes just before
```

#### Example 27: modifying immutables
``` python
# remove vowels

message = input("message:")
new_message = ""
VOWELS = "aeiou"

print()
for letter in message:
    if letter.lower() not in VOWELS:
        new_message += letter
        print("new string created:", new_message)

print("message without vowels:", new_message)
```

### Constants
- conventionally, names in all caps refer to stuff meant to keep constant throughout the program
    - constants are convenient
    - can be used at the beginning of a program to indicate some parameter that recurs within the program that may be changed at a later date
    - warning: constants aren't constants in py
    - the caps are only indicating something is a constant to a human reading the program

### Slicing sequencing
- can extract a subsequence from a sequence using the subsequence's range
- can use positive or negative notation to give ranges from beginning to end or vice versa
- word[x:y]

#### Example 28
``` python
print("enter beginning and ending index for your slice of pizza")
print("press enter key at start to exit")

word = "pizza"

start = None
while start != "":
    start = (input("start:"))
    
    if start:
        start = int(start)
        
        finish = int(input("finish:"))
        
        print("word[", start, ":", finish, "] is", end=" ")
        print(word[start:finish])
        
input("enter to exit")
```


