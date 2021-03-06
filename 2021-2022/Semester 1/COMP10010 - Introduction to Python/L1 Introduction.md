# L1: Introduction
[COMP10010_02.pdf](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/91a4565b-cd4f-4c49-8ed2-ae9a9f08f8da/COMP10010_02.pdf)
###### tags: `COMP10010 - Introduction to Python`

## **Programming:** 
“The process of designing, writing, testing, debugging, and maintaining the source code of computer programs.”
“The purpose of programming is to create a set of instructions that computers use to perform specific operations or to exhibit desired behaviors.” [Wikipedia]

#### **Compiler:** a compiler translates a program written in programming language (like Python) into the language spoken by your computer.
• You will need a compiler for this course.
• You can get one for free here:
• https://www.python.org/downloads/

#### **IDLE modes:**

Interactive: scratchpad for testing quick single-lines

Script mode: writing longer code to be saved, expanded later on, etc.

### **Comments:**

- in python, everything following the # sign (on the same line) is considered a comment and ignored when translating the program into computer language (compiling)
    
    ```python
    # this is a comment
    ```
    
- comments can explain what certain segments of code are doing or how they are executing their functions
    - helpful for self (looking back at old code)
    - helpful for someone else looking at code (to quickly gauge what's going on)
    

### **User-input: (interactivity)**

e.g. rather than exiting program immediately, have user read what program did and exit after a key is pressed (python files automatically run and close after being clicked on → this allows user to see what happened before having it close)

```python
print("this prints a line of text")
input("\n\npress enter to exit")

# input prints string given and waits for user to press interact
```

### **print() and input():**

- print("something") prints "something" and moves on
- input("something") also prints "something", but then waits for user to interact, after which it moves on

#### **print();**

##### Escape sequences:

| Escape sequence | Function |
| -------- | -------- | 
|\\\       |\         | 
|\\'       |'         |
|\\"       |"         |
|\\a       |bell      |
|\\b       |backspace |
|\\n       |new line  |

##### Multiple lines:

```python
print("string 1", "string 2", "string 3")
```

#### Ending a print:
- normally a print statement does 2 things
    - adds spaces between different strings
    - adds a new line character at the end of the last string
    - if you want to use a different ending, you can use end=
    
        ```python
        print("here it is", end="different ending")
        ```    

#### Formatting bigger strings:

- use triple """ """
    
    ```python
    print("""
    	anything between the triple quotes prints as is
    	with this exact formatting
    """)
    ```

#### String concatenation:

- use plus +
    
    ```python
    print("th"+"is")
    ```
    
#### Stretching statements over multiple lines:

- use back-slash \
    
    ```python
    print("on line 1" \ + "on line 2")
    ```
    
#### Repeating strings:

- use multiplication *
    
    ```python
    print("10 times"*10)
    ```
