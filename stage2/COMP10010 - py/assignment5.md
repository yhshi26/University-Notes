# Assignment 5
###### tags: `COMP10010 - py`

``` python
# read 1000 floats from a file (floats.txt) into a list
# create a function insertion_sort(float_list) that takes as argument a list of floating point numbers and sorts it in ascending order (smallest first) using the Insertion Sort algorithm 
# after reading the floats from the file into a list, your main program should call the insertion_sort function, then it should:
# 1) print the now sorted list onto the screen;
# 2) write the sorted list onto a file (sorted_floats.txt)

import sys

def insertion_sort(float_list, order):
    for i in range(1, len(float_list)):
        temp = float_list[i]
        j = i-1
        if (order == "ascending"):
            while j >= 0 and temp < float_list[j]:
                float_list[j+1] = float_list[j]
                j -= 1
        else:
            while j >= 0 and temp > float_list[j]:
                float_list[j+1] = float_list[j]
                j -= 1
        float_list[j+1] = temp

def selection_sort(float_list, order):
    for i in range(len(float_list)):
        index = i
        for j in range(i+1, len(float_list)):
            if (order == "ascending"):
                if float_list[index] > float_list[j]:
                    index = j
            else:
                if float_list[index] < float_list[j]:
                    index = j       
        float_list[i], float_list[index] = float_list[index], float_list[i]

def partition(start, end, float_list, order):
    index = start
    pivot = float_list[index]
    
    while start < end:
        if order == "ascending":
            while start < len(float_list) and float_list[start] <= pivot:
                start += 1
            while float_list[end] > pivot:
                end -= 1
            if (start < end):
                float_list[start], float_list[end] = float_list[end], float_list[start]
        else:
            while start < len(float_list) and float_list[start] >= pivot:
                start += 1
            while float_list[end] < pivot:
                end -= 1
            if (start < end):
                float_list[start], float_list[end] = float_list[end], float_list[start]
    
    float_list[end], float_list[index] = float_list[index], float_list[end]
    
    return end
        
def quick_sort(start, end, float_list, order): 
    if (start < end):
        s = partition(start, end, float_list, order)
        quick_sort(start, s-1, float_list, order)
        quick_sort(s+1, end, float_list, order)
               
# main
print("opening floats.txt, reading floats into a list...")
text_file = open("floats.txt", "r")
lines = text_file.readlines()
float_list = []
for line in lines:
    line = line.strip()
    float_list.append(float(line))

text_file.close()

print("this program has 3 built-in sorting functions including: insertion, selection, and quick sort (not that they will change results, but they have different time complexities!)")

while True:
    order = input("sort floats ascending or descending? ")
    if order.lower() not in ("ascending", "descending"):
        print("not an appropriate choice, valid responses include: ascending, and descending")
    else:
        break

while True:
    sort_type = input("sort floats using insertion, selection, or quick sort? ")
    if sort_type.lower() not in ("insertion", "selection", "quick"):
        print("not an appropriate choice, valid responses include: insertion, selection, and quick")
    else:
        break

print("sorting...")
        
if sort_type == "insertion":
    insertion_sort(float_list, order)
    print("the time complexity of insertion sort is O(n) in the best case, and O(n^2) otherwise")
elif sort_type == "selection":
    selection_sort(float_list, order)
    print("the time complexity of selection sort is always O(n^2)")
else:
    quick_sort(0, len(float_list)-1, float_list, order)
    print("the time complexity of quick sort is in the best case/on average O(n log(n)), and O(n^2) in the worst case")
    
print("floats sorted in", order, "order using", sort_type, "sort:")
text_file2 = open("sorted_floats.txt", "w")
print(float_list)
for i in range(len(float_list)):
    # print(float_list[i])
    text_file2.write(str(float_list[i])+"\n")
text_file2.close()
    
print("floats have been written to sorted_floats.txt")
input("press enter to terminate program")
```
