# L12: Lists and sorting algorithms
[COMP10010_13](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1693047/View)
###### tags: `COMP10010 - Introduction to Python`

> assignment 4: function to check if user input string is palindrome (reads same backwards/forwards), must use indexing, no existing py functions excluding upper() and lower(), function should return palindrome info (no print), code should repeat (ask user if want to check another word)

> last lect: recursive functions (e.g. fibonacci series), sorting, tuples (```tuple = ()```) vs lists (```list = []```), list functions (```len()```,```in```, indexing, slicing, concatenating) and functionality beyond tuple functionality (lists are mutable, tuples are immutable)

#### Example 32
``` python
# high scores
# demonstrates list methods

scores = []
choice = None
while choice != "0":
    print(
    """
    high scores
    
    0 - exit
    1 - show scores
    2 - add a score
    3 - remove a score
    4 - sort scores
    """)

choice = input("choice: ")
    print()
    
    # exit
    if choice == "0":
        print("bye")
    
    # list high-score table
    elif choice == "1":
        print("high scores:")
        for score in scores:
            print(score)
    
    # add a score
    elif choice == "2":
        score = int(input("what score did you get?: "))
        score.append(score)
        
    # remove a score
    elif choice == "3":
        score = int(input("remove which score?: "))
        if score in scores:
            scores.remove(score)
        else:
            print(score, "isn't in high scores list")
    
    # sort scores
    elif choice == "4":
        scores.sort(reverse=True)
    
    # some unknown choice
    else:
        print("sorry, but", choice, "isn't valid")
    
input("\npress enter to exit")
```

## Methods for lists
- append(): add
- remove(): remove
- sort(): sort
- sort(reverse=True): sort backwards

#### Example 30xb
``` python
import random

N = int(input("how many random numbers?: "))

seq_num = []
for i in range(0,N):
    seq_num += random.randrange(0,100)

print("here is your random sequence:")
print(seq_num)

sorted_seq_num = []

for i in range(0,N):
    maxv = 0
    maxp = -1
    for j in range(0,len(seq_num)):
        if seq_num[j]>maxv:
            maxv = seq_num[j]
            maxp = j
    sorted_seq_num += seq_num[maxp],
    del seq_num[maxp]

print("sorted:")
print(sorted_seq_num)
```

#### Example 30y: bubble sort
``` python
# bubble sort
import random

N = int(input("how many random  numebrs?: "))
seq_num = []

for i in range(0,N):
    seq_num += random.randrange(0,100),
    
print("here is your random sequence:")
print(seq_num)

for i in range(0,N):
    for j in range(0,N-1-i):
        if seq_num[j]>seq_num[j+1]:
            temp = seq_num[j]
            seq_num[j] = seq_num[j+1]
            seq_num[j+1] = temp

print("sorted:")
print(seq_num)
```

### Tuples vs lists
- if lists can do everything tuples can do and more, why use tuples?
    - tuples are faster
    - tuples are immutable so they make better constants
    - sometimes you need tuples (in dictionaries), we'll see that

### Nested sequences
- you can have sequences within sequences
- you can have tuples or lists within tuples or lists
- while it gets confusing quite quickly, it can be handy in some cases so long as you keep to a couple levels at most (as you could, for instance,  have tuples within tuples within tuples)





