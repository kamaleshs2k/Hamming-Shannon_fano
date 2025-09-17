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
### 1) Average codeword length L = ∑ p_k * l_k

Terms p_k * l_k:
- 0.125 * 3 = 0.375
- 0.0625 * 4 = 0.25
- 0.25 * 2 = 0.5
- 0.0625 * 4 = 0.25
- 0.125 * 3 = 0.375
- 0.125 * 3 = 0.375
- 0.25 * 2 = 0.5

Sum: L = 2.625

---

### 2) Entropy H = ∑ p_k * log2(1/p_k)

- p = 0.125 → log2(1/0.125)=3 → 0.125*3 = 0.375
- p = 0.0625 → log2(1/0.0625)=4 → 0.0625*4 = 0.25
- p = 0.25 → log2(1/0.25)=2 → 0.25*2 = 0.5
- p = 0.0625 → same as above → 0.25
- p = 0.125 → same as first → 0.375
- p = 0.125 → same → 0.375
- p = 0.25 → same as third → 0.5

Sum: H = 2.625

---

### 3) Efficiency and Redundancy
- Efficiency = H / L = 2.625 / 2.625 = 1.0 = 100%
- Redundancy = 1 - efficiency = 0.0

---

### 4) Variance of codeword length Var = ∑ p_k * (l_k - L)^2

- l=3 → (3-2.625)^2=0.140625 → *0.125 = 0.017578
- l=4 → (4-2.625)^2=1.890625 → *0.0625 = 0.118164
- l=2 → (2-2.625)^2=0.390625 → *0.25 = 0.097656
- l=4 → same as above → 0.118164
- l=3 → same as first → 0.017578
- l=3 → same → 0.017578
- l=2 → same as third → 0.097656

Sum: Var = 0.484

---

### Final Results
- Average Codeword Length L : 2.625
- Entropy H : 2.625
- Efficiency : 100%
- Redundancy : 0.0
- Variance : 0.484

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
