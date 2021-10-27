# Assignment 3
###### tags: `COMP10010 - py`
``` python
# Write a program that: 1. user input number N;
# 2. all prime numbers between 1 and N inclusive print to screen;
# 3. sum of squares of all prime numbers between 1 and N 
# inclusive computed and print to screen;
# 4. user asked if they want to compute new sum of squared numbers, if yes, repeat

print("this program takes an input integer N and interates from 1 to N,")
print("printing all prime numbers in the range (inclusive)")    
print("and a sum of the squares of all prime numbers in the range")

compute = "y"

while "y" in compute.lower():
    primes = ""
    sum = 0
    
    N = int(input("input N: "))
    
    for num in range(2, N + 1):
        # 1 is not a prime -> only has 1 divisor
        # a prime has 2 divisors, 1 and itself
        for i in range(2, num):
            if (num % i) == 0:
                break
        else:
            primes += str(num) + " "
            sum += num*num
    
    print("primes between 1 and ", N, ": ", primes)
    print("sum of squares of primes between 1 and ", N, ": ", sum)
    
    compute = input("compute new sum of squared numbers? (Y/N): ")
    
print("program terminating")          
```
