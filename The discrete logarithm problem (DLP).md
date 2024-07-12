---
tags:
  - Concept
  - criptografía
Sumary: Considered a difficult problem to solve, especially for large numbers, which makes it useful for cryptography. Given a prime number p, a generator g, and a value y, find the integer x such that g^x ≡ y (mod p)
---

# MOC
* [[Concepts MOC]]
# Related notes

```dataview
TABLE WITHOUT ID link(file.name) AS "Nota", file.cday AS "Created date" , Sumary
WHERE contains(file.outlinks, this.file.link)
OR contains(file.inlinks, this.file.link)
and !contains(file.name , "MOC")
AND file.name != this.file.name
```

# Resources:
* Video: https://www.youtube.com/watch?v=za9azzh4v9A
# Description 
![[Pasted image 20240701103602.png|600]]


```python
#Generate elements of (Z_7)^{x} using generator [5].
g = 5
p = 7
print(f"Using generator {g}")
for k in range(3*p):
    print(f"{g}**{k} mod {p} ≡ {(g**k)%7}")
```
![[Pasted image 20240701104037.png|200]]
![[Pasted image 20240701104418.png|600]]

# Discrete Logarithm Problem (DLP)

## Definition
- Given a prime number p, a generator g, and a value y, find the integer x such that g^x ≡ y (mod p)
- The problem is to find the **discrete logarithm x of y to the base g modulo p**
## Key Components
### Finite Cyclic Group
- DLP is defined in a finite cyclic group
- The group is formed by the set of integers modulo p, denoted as Z_p
- The group operation is modular multiplication
### Generator
- An element g in Z_p is called a generator if every element in Z_p can be expressed as a power of g
- The order of g is the smallest positive integer n such that g^n ≡ 1 (mod p)
### Discrete Logarithm
- The discrete logarithm of y to the base g modulo p, denoted as log_g(y) mod p, is the integer x such that g^x ≡ y (mod p)
## Principles
### Computational Complexity
- DLP is believed to be a computationally hard problem
- No efficient classical algorithm is known to solve DLP in general
- The best known classical algorithms have exponential time complexity
### Cryptographic Hardness
- The hardness of DLP is the basis for the security of many cryptographic systems
- Widely used in public-key cryptography, such as the Diffie-Hellman key exchange and the ElGamal encryption system
## Potential Applications
### Cryptography
- Public-key cryptography
- Digital signatures
- Key exchange protocols
## Quantum Computing
- **Shor's algorithm can solve DLP in polynomial time on a quantum computer**
- Poses a threat to cryptosystems based on DLP