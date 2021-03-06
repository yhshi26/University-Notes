# L6: Pseudocode
[COMP10010_07](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1661171/View)
###### tags: `COMP10010 - Introduction to Python`

> last lect: while loops, sentries (a variable a while loop's condition can depend on), infinite loops (and intentional infinite loops), values as conditions (numbers false if 0, true otherwise; strings false if empty "", true otherwise), using break and continue, truth tables 

## Planning a program
> should you? short answer: yes
>
> we have a tendency to try to fix things rather than throwing them away and starting again

### How to plan a program
- protocols and techniques have been devised to aid in efficiently (and collaboratively) planning a program 
    - sketch on paper using literal language ("pseudocode")
    - re-sketch, incorporate some code (e.g. put loops in it) but keep it loose (e.g. say "do thing X")
    - refine, iteratively
        - if the program is complex enough, some statements in the first program-like sketch will be somewhat complex to implement (e.g. "sort the values in descending order")
        - this should be, in a second phase, extended to a list of steps (an algorithm)

### Algorithms
- an algorithm (from the Persian mathematician Mohammed ibn-Musa al-Khwarizmi, محمد بن موسى الخوارزمی), is a sequence of steps to be taken to do something, i.e. solve a problem
    - with sketches (especially the second version that looks almost like code), you are essentially coming up with the algorithm to solve your problem

### Example: guessing a number
- program will ask user to guess a number
- keep asking user for new guess until correct number input
- give user some hint of what went wrong

#### Pass 0
- pick a random number
- ask user to guess, keep asking until correct input
- let user know they guessed correctly

#### Pass 1
- pick a random number
- while user guess incorrect
    - let user guess
- let user know they guessed correctly

#### Pass 2
- intro
- pick a random number N between 1 and 100
- ask user for guess
- while user's guess != N
    - if guess < N
        - tell user to guess higher
    - else
        - tell user to guess lower
    - let player guess
    - number guesses ++
- let user know they guessed correctly
- tell user number guesses taken

#### Program
``` python
# guess number
# computer picks number between 1 and 100
# user guesses number, computer gives hints (guess higher/lower)
# computer tells user if they are correct and number guesses taken

import random

print("Guess number game")
n = random.randint(1,100)
n_user = int(input("Guess:"))
num_guesses = 1
while n_user != n:
    if (n_user < n):
        print("Higher")
    else:
        print("Lower")
    n_user = int(input("Guess:"))
    num_guesses += 1
print("Correct guess, number guesses taken", num_guesses)
```
### Example: flipping coin and loops
- want to check if py's random generator works
- to do so, write program that flips a coin many times to see if roughly same number heads and tails returned

``` python
# multiple coin flip program
# check whether random generator really is random

import random

print("this program flips coin many times")
print("computes heads/tails distribution stats")

times = int(input("input number flips"))

counter = 0
tails = 0

while counter < times:
    flip = random.randint(0,1)
    if flip:
        tails = tails + 1
    counter += 1

stats = 100.0*tails/times

print("tails:" + str(stats) + "%, heads:" + str(100-stats) + "% of the time")
```



