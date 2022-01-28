# Assignment 2
###### tags: `COMP10010 - Introduction to Python`

``` python
# Write a program that: 1. asks the user their name; 
# 2. asks them their height in centimetres; 
# 3. converts the height into feet, inches and quarter inches; 
# 4. prints out a message saying: “Dear NAME you are F ft I Q/4 in tall” 
# (where: NAME is the name of the user all in uppercase, 
# F, I and Q are, respectively, the feet, inches and quarter inches of the user’s height)

name = input("Input name:")
height_cm = int(input("Input height in cm:"))

F = int(height_cm/30.48)
I = int((height_cm%30.48)/2.54)
Q = int(((height_cm%30.48)/2.54-I)*4)

print("Dear", name.upper(), "you are", F, "ft", I, Q, "/4 in tall")

```

