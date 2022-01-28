# L14: Reading and writing to files
[COMP10010_15](https://brightspace.ucd.ie/d2l/le/content/129818/viewContent/1703462/View)
###### tags: `COMP10010 - Introduction to Python`

> last lect: accessing nested elements, unpacking, functions and abstraction, practical abstraction, encapsulation
> note: once you specify one default parameter in the function definiteion you have to specify all of them

## Files
- we have seen plenty of cases when it would be helpful to access files
- e.g. you want a dictionary of words for the word jumble game and don't want to have to type them all in your program
- or you want to process some data coming from an external source; it is a real pain to have to type it inside your code
- py (just like any other language) gives you plenty of ways to read and write files
    - simplest type of file is text file, one that can be opened in a notepad or similar and read (isn't encoded in any gibberish)
    - text files are great because you can easily edit them from outside your program

#### Example 45
``` python
# read and print contents of a text file

text_file = open("words.txt", "r")
print(text_file.read())
text_file.close()
```

#### Example 46
``` python
text_file = open("words.txt", "r")
whole=text_file.read()
text_file.close()
print(whole)

text_file = open("words.txt", "r")
list1=text_file.readlines()
text_file.close()
for 1 in list1:
    print(1)
    
text_file = open("words.txt", "r")
list2=text_file.read().splitlines()
text_file.close()
for 1 in list2:
    print(1)
```

## Writing onto files
- equally easy as reading from them (especilaly text files)
- very handy, as anything produced by a program can be saved (for potentially future use)

#### Example 47
``` python
# demonstates writing to a text file

print("creating a text file with the write() method")
text_file = open("write_it.txt", "w")
text_file.write("line 1\n")
text_file.write("line 2\n")
text_file.write("line 3\n")
text_file.close()

print("\nreading new file")
text_file = open("write_it.txt", "r")
print(text_file.read())
text_file.close()

print("\ncreating a text file with the writelines() method")
text_file = open("write_it.txt", "w")
lines = ["line 1\n", "line 2\n", "line 3\n"]
text_file.writelines(lines)
text_file.close()

print("\nreading new file")
text_file = open("write_it.txt", "r")
print(text_file.read())
text_file.close()

input("\npress enter to exit")
```

### ```write``` likes strings
- error example
    - ![](https://i.imgur.com/AbcmtpC.png =350x)
- fix
    - ![](https://i.imgur.com/TxW5d8j.png =350x)





