# NAME:VARSHINI M

# REGISTER NUMBER:212224060293

# EXP N0-2 Huffman-Shannon_fano

# Aim:

Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
1.Personal Computer

2.Google Colab
# Program:
```
#Huffman and Shannon-Fano coding
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:
<img width="450" height="1239" alt="image" src="https://github.com/user-attachments/assets/2ccdf2f9-fe7a-4ca8-b472-6581d259ac7b" />

<img width="450" height="1239" alt="image" src="https://github.com/user-attachments/assets/02c9f7b6-71f2-4318-be28-a3ac4c970e09" />


# Output

<img width="522" height="377" alt="image" src="https://github.com/user-attachments/assets/94bd6054-9ef5-498f-973f-9a2f7bc8259c" />



# Results:

The Huffman and Shannon-Fano of the given statistics {0.4,0.2,0.2,0.1,0.1} using python are verified.

