---
tags:
  - Concept
  - criptografía
Sumary: KEM is a cryptographic protocol used to securely establish a shared secret key between two parties over an insecure channel
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


# Description 

* [[Introduction a Quantum Safe#KEMs Key encapsulation Mechaninsim]]

Key Encapsulation Mechanism (KEM) in a way that's easy to understand for someone new to the subject.

I. Introduction to Key Encapsulation Mechanism (KEM)
   A. Definition: KEM is a cryptographic protocol used to securely establish a s**hared secret key between two parties over an insecure channel.**

II. How KEM Works
   A. **Key Generation**
      1. The sender generates a **public-private key pair** using a specific mathematical algorithm.
      2. The **public key is shared with the intended recipient**, while the private key is kept secret.

   B. **Key Encapsulation**
      1. The **sender uses the recipient's public key to generate a random symmetric key** (the shared secret key) and **an encapsulated key.**
      2. The **encapsulated key is sent to the recipient over an insecure channel**.

   C. Key **Decapsulation**
      1. The r**ecipient uses their private key to decapsulate the encapsulated key** received from the sender.
      2. This process allows the **recipient to recover the shared secret key**.

   D. Secure **Communication**
      1. **Once both parties have the shared secret key**, they can use it to securely communicate or encrypt data using symmetric-key cryptography.
![[Pasted image 20240624125815.png|500]]
*The random symmetric key generated during the key encapsulation step and the key obtained after the key decapsulation step are the same. ?*

III. Advantages of KEM
    A. Separates Key Establishment and Data Encryption
       1. KEMs are designed **specifically for secure key establishmen**t, while **data encryption is handled separately using symmetric-key cryptography.**
       2. This separation of concerns allows for more flexibility and potential performance improvements.
	B. Resistance to Quantum Attacks
       1. Some **KEM algorithms, such as those based on lattice-based cryptography, are believed to be resistant to attacks by quantum computers.**
       2. This makes KEMs an attractive choice for future-proofing secure communication systems.
    C. Efficiency and Scalability
       1. KEMs can be more efficient than traditional key exchange methods, especially in scenarios involving a large number of participants.
       2. They can be easily scaled to accommodate different security levels and key sizes.

IV. Examples of KEM Algorithms
    A. ECIES (Elliptic Curve Integrated Encryption Scheme)
    B. CRYSTALS-Kyber (based on lattice-based cryptography)
    C. SIKE (Supersingular Isogeny Key Encapsulation)
