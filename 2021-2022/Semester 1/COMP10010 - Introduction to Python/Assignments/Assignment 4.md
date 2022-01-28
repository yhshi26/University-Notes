# Assignment 4
###### tags: `COMP10010 - Introduction to Python`
``` python
# Write a function to check if a string is a palindrome
# function must: 1: use indexing
# 2: use no existing py functions (excluding upper() and lower()) within the function
# 3: not print info, return

# pass in length because cannot use existing py functions other than upper() and lower() in function
def is_palindrome(string, length):
    for i in range(0, int(length/2)):
        if string[i] != string[length-i-1]:
            return False
    return True

check = "y"

while "y" in check.lower():
    string = input("string to check: ").lower()
    if is_palindrome(string,len(string)):
        print(string, "is a palindrome")
    else:
        print(string, "is not a palindrome")
    
    check = input("check if another word is a palindrome? (Y/N): ")
    
print("program terminating")
```
