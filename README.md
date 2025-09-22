### Date  :17-09-2025
### Name  : KAMALESH S
### Reg.no: 212223060108
# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
### GOOGLE COLAB
# Program:
```python
#Huffman-Shannon_fano
import math
# Probabilities given
p = [0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25]
# Corresponding Huffman/Shannon-Fano code lengths
lk = [3, 4, 2, 4, 3, 3, 2]
n = len(p)
# Average Codeword Length
L = sum(p[k] * lk[k]
for k in range(n))
# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2)
 for k in range(n))
hs = round(hs, 3)
# Efficiency & Redundancy
eff = round(hs / L, 3)
red = round(1 - eff, 3)
# Variance of codeword length
var = sum(p[k] * (lk[k] - L) ** 2
for k in range(n))
var = round(var, 3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:
<img width="1251" height="1080" alt="image" src="https://github.com/user-attachments/assets/a634e844-81e4-4998-81f8-eedcd485e799" />


# Output
```yaml
Average Codeword Length is : 2.625
Entropy is : 2.625
Efficiency is : 100.0%
Redundancy is : 0.0
Variance is : 0.484
``` 
# Results:

Thus, the output for Huffman-Shannon_fano hasbeen Verified successfully.
