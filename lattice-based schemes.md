---
tags:
  - Concept
  - criptografía
Sumary: cryptographic construction that relies on the hardness of problems related to lattices, which are mathematical objects that can be thought of as a regular arrangement of points in a multi-dimensional space.
---
****
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


# Description 

Lattice-based schemes are a type of cryptographic construction that relies on the **hardness of problems related to lattices, which are mathematical objects that can be thought of as a regular arrangement of points in a multi-dimensional space.**

In the context of cryptography, lattice-based schemes are often used to build secure cryptographic primitives, such as public-key encryption schemes, digital signatures, and cryptographic hash functions. The security of these schemes relies on the difficulty of solving certain problems related to lattices, such as:

1. *test Vector Problem (SVP)**: Given a lattice, find the shortest non-zero vector in the lattice.
2. **Closest Vector Problem (CVP)**: Given a lattice and a target vector, find the closest vector in the lattice to the target vector.
3. **Learning With Errors (LWE)**: Given a set of noisy linear equations, find a solution that satisfies the equations. [[Introduction a Quantum Safe#LATTICE-BASED CRYPTOGRAPHY 101]]

Lattice-based schemes have several attractive features, including:

1. **Post-quantum security**: Lattice-based schemes are thought to be resistant to attacks by quantum computers, making them a promising candidate for post-quantum cryptography.
2. **Efficiency**: Lattice-based schemes can be more efficient than other cryptographic constructions, especially for certain types of computations.
3. **Flexibility**: Lattice-based schemes can be used to build a wide range of cryptographic primitives, including public-key encryption schemes, digital signatures, and cryptographic hash functions.

Some popular lattice-based schemes include:

1. **NTRU**: A public-key encryption scheme that uses a lattice-based construction to achieve security.
2. **Ring-LWE**: A variant of LWE that uses a ring structure to improve efficiency and security.
3. **BLISS**: A digital signature scheme that uses a lattice-based construction to achieve security and efficiency.
4. **Falcon**: A lattice-based cryptographic hash function that is designed to be highly secure and efficient.

The advantages of lattice-based schemes include:

1. **Improved security**: Lattice-based schemes can offer improved security compared to other cryptographic constructions, especially against quantum attacks.
2. **Better performance**: Lattice-based schemes can offer better performance compared to other cryptographic constructions, especially for certain types of computations.
3. **Flexibility**: Lattice-based schemes can be used to build a wide range of cryptographic primitives, making them a versatile tool for cryptographic applications.

However, lattice-based schemes also have some challenges and limitations, including:

1. **Complexity**: Lattice-based schemes can be complex and difficult to implement, especially for non-experts.
2. **Key sizes**: Lattice-based schemes often require large key sizes to achieve security, which can be a challenge for certain applications.
3. **Side-channel attacks**: Lattice-based schemes can be vulnerable to side-channel attacks, whicy if not properly mitigated.

In summary, lattice-based schemes are a powerful tool for building secure cryptographic primitives, offering improved security, better performance, and flexibility. However, they also require careful implementation and consideration of their limitations to ensure security in practice.


# Related notes

[[4. Quantum-safe cryptography#Lattice-based cryptography]]