# L5: Logic
[COMP10010_06](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1652660/View)
###### tags: `COMP10010 - Introduction to Python`

> last lect: random module (random.randint(a,b), random.randrange(a,b)), control (if, elif, else), indentation and blocks

## Repeating things: loops
- repeat a line/lines of code multiple times
- "loops are our friends"

### while loops
``` python
# repeats thing X, so long as condition remains true
while condition:
    do thing X
```

### Example 15
``` python
# 3 year-old simulator
# demonstrates the while loop

print("\tWelcome to the 'Three-Year-Old Simulator'\n")
print("This program simulates a conversation with a three-year-old child.")
print("Try to stop the madness.\n")

response = ""
while response != "Because.":
    response = input("Why?\n")

print("Oh.  Okay.")
input("\n\nPress the enter key to exit.")
```
### Example 16 - infinite loops
``` python
# never meets condition
# demonstrates infinite loop

choice = 1
while choice = 1:
    print("x")
```

### Sentries
- a while loop's condition can depend on a variable
    - this variable is called the condition
    - the sentry is compared to something else
- make sure sentries are initialized
    - assign them a value such that they do what you want the first time your program gets into the loop
    - or, make the user input something in the sentry
- make sure your condition will eventually become false, else infinite loop

## Values as conditions
- in py (and many other programming languages), conditions can take on odd forms
    - e.g. ```if 35:``` and ```while "hi":```

## In general
- numbers (float and int) evaluate to false if they are 0 and true otherwise
- strings evaluate to false if they are empty ("") and true otherwise
``` python
if var:
# this is the same as
if var != 0
```

## Intentional infinite loops
- sometimes it's helpful to have what is apparently an infinite loop where the condition is always true
- there are other ways to exit a loop which don't involve tampering with the condition, which is sometimes more elegant to use
``` python
# a counter
# demonstrates the break and continue statements

count = 0
while True:
    count += 1
    # end loop if count > 10
    if count > 10:
        break
    # skip 5
    if count == 5:
        continue
    print(count)

input("\n\nPress the enter key to exit")
```

### Notice
- while ```break``` and ```continue``` are useful, they (especially the former) acan make a program harder to follow
    - what gets you out of a loop is no longer confined to the condition - it can be anywhere

## Compound conditions
- you can combine conditions using logical operators
    - e.g. condition1 and condition2

### Example 19
``` python
# exclusive network
# demonstrates logical operators and compound conditions

print("\tExclusive Computer Network")
print("\t\tMembers only!\n")

security = 0
username = ""

while not username:
    username = input("Username: ")
    password = ""
while not password:
    password = input("Password: ")

if username == "M.Dawson" and password == "secret":
    print("Hi, Mike.")
    security = 5
elif username == "S.Meier" and password == "civilization":
    print("Hey, Sid.")
    security = 3
elif username == "S.Miyamoto" and password == "mariobros":
    print("What's up, Shigeru?")
    security = 3
elif username == "W.Wright" and password == "thesims":
    print("How goes it, Will?")
    security = 3
elif username == "guest" or password == "guest":
    print("Welcome, guest.")
    security = 1
else:
    print("Login failed.  You're not so exclusive.\n")

input("\n\nPress the enter key to exit.")
```

### ```not```
``` python 
username = ""

while not username:
    username = input("Username: ")
```
This keeps asking for a user name until one enters one other than the empty string. Remember: the empty string is false. ```not``` inverts the truth of a condition. It is a unary operator (it works on one thing).

### ```and```
``` python
username == "M.Dawson" and password == "secret":
    print("Hi, Mike.")
```
The ```and``` logical operator combines two conditions. The combination is true if and only if both conditions are true. It is a binary operator (it works on two things).

### ```or```
``` python
elif username == "guest" or password == "guest":
    print("Welcome, guest.")
    security = 1
```
```or``` returns true if either condition is true. It is a binary operator.

## Truth tables
| A | B | A and B | A or B | not A |
| - | - | ------- | ------ | ----- |
| false | false | false | false | true |
| false | true | false | true | true |
|true | false | false | true | false |
|true | true | true | true | false|



