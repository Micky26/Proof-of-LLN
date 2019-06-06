# Proof-of-LLN
import numpy as np
from numpy.random import randn

#Method 1

N = 10000                #set the Number of Random Variables to generate.
x = randn(N)             #declare a variable that generates the Random numbers.
valid = []               #append all numbers that fall btw -1 and 1.
for X in x:              #loop over all randomly generated numbers to determine mubers that fall btw -1 and 1 and append to valid.
    if X > -1 and X < 1:
        valid.append(X)
print(len(valid)/N)      #calculate the mean and print.


#Method 2

counter = 0             #Initialize a counter that only increases when condition is met.
N = 10000               #set the Number of Random Variables to generate.
x = randn(N)            #declare a variable that generates the Random numbers.
for X in x:             #loop over all randomly generated numbers to determine mubers that fall btw -1 and 1,counter increases when condition met.
    if X > -1 and X < 1:
        counter  = counter + 1
print(counter/N)        #calculate the mean and print.

