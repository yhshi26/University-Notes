# L13: Abstraction
[COMP10010_14](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1696607/View)
###### tags: `COMP10010 - Introduction to Python`

> last lect: methods for lists (```list.append(something)```, ```list.remove(something)```, ```list.sort()```, ```list.sort(reverse=True)```), bubble sort, tuples vs. lists, nested sequences

#### Example 39
``` python
# high scores 2.0
# demonstrates nested sequences

scores = []
choice = None
while choice != "0"
    print(
    """
    high scores 2.0
    
    0 - quit
    1 - list scores
    2 - add a score
    """
    )

choice = input("choice: ")
    print()
    
    # exit
    if choice == "0":
        print("terminating")
    
    #display high-score table
    elif choice == "1":
        print("high scores\n")
        print("name\tscore")
        for entry in scores:
            score, name = entry
            print(name, "\t", score)

    # add a score
    elif choice == "2"
        name = input("name: ")
        score = int(input("score:"))
        entry = (score, name)
        scores.append(entry)
        scores.sort(reverse=True)
        # keep only top 5 scores
        scores = scores[:5] 
    
    # some unknown choice
    else:
        print("sorry,", choice, "is not valid")

input("\npress enter to exit")
```

#### Example 40
``` python
import math

def sum_sqrt(N):
    tot = 0
    for i in range(1,N+1):
        tot += math.sqrt(i)
    return tot

# main program

r = int(input("number rows: "))
c = int(input("number columns: "))

matrix = [[0 for x in range(c)] for y in range(r)]

for i in range(r):
    for j in range(c):
        matrix[i][j] = sum_sqrt(i+j)

print(matrix)

for i in range(r):
    for j in range(c):
        print("{0:.3f}".format(matrix[i][j])), end="\t")
    print("\n")

input("type a key")
```

## Functions and abstraction
- when you write a function, you are doing abstraction
    - in this context, you indentify a high level task to be performed and don't worry about the details of how it is done
    - or rather, that worry about details is separated to a different session (or person)

### Practical abstraction
- once you have abstracted, you genuinely stop worrying about the function embodying the abstract concept
- you can write a program that calls a function when the function hasn't been writen yet
    - you simply need an empty shell for the function and it will compile and run
- obviously, the key is coming up with good abstractions (think before writing)

### Encapsulation
- what happens in a functions stays in the function
- you have limited, well defined ways to interact with a function (parameters, return values), and that is useful
    - it is encapsulated 

#### Encapsulation is useful
- without it, if a function is not well encapsulated, it can mess up variables in the code that calls it, resulting in unintentional errors in the code
- encapsulation cooperates with encapsulation
    - abstraction needs encapsulation to work well in practice
    - you can abstract as much as you want, but you can't stop worrying about the function if it's not well encapsulated

### Keyword arguments and default parameters
- it is possible to specify default arguments to functions
    - that is, values for parameters that apply whenever the parameter is not set by the function user
- keyword arguments, instead, are a different way to give arguments to a function by specifying which one of the parameters they refer to (useful if more than one..)

#### Example 41
``` python
# student scores
# demonstrates keyword arguments and default parameter values

# positional parameters
def score1(name, score):
    print("hi,", name, ", you received:", score)
    
# parameters with default values
def score2(name = "jack", score = 3.14):
    print("hi,", name, ", you received:", score)
    
score1("jack", 3.14)
score1(3.14, "jack")
score1(name = "jack", score = 3.14)
score1(score = 3.14, name ="jack")

score1()
score1(name = "senpai")
score1(score = 6.28)
score1(name = "senpai", score = 6.28)
score1("senpai", 6.28)
    
input("\npress enter to exit")
```
