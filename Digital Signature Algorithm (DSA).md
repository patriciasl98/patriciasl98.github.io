---
tags:
  - Concept
  - criptografía
Sumary: "A cryptographic algorithm used for digital signatures\r- Provides data integrity and authentication"
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
Sure, I can help you create a mind map that connects the concepts explained in the Digital Signature Algorithm (DSA) and helps someone understand it in a visual way. Here's a mind map that covers the key concepts of DSA:
This scheme, which came to be known simply as the _Digital Signature Algorithm_ (DSA), involves four distinct phases:

1. **Key generation**:
	DSA keys are generated from:

	- **2 primes** that meet certain rules
	    - 𝑝 - typically 256 bits (we'll call this length 𝑁)
	    - 𝑞- typically 3072 bits (we'll call this length 𝐿)
	- A cryptographic **hash function that will convert from strings of length 𝐿 to 𝑁**
	- An additional Parameters 𝑔 (see details below)

![[Pasted image 20240701115617.png|500]]

2. **Key distribution:**
    
    The following information is shared with anyone who wishes to validate a signature
    
    - The parameters used (𝑝,𝑞,𝑔)(p,q,g) which describe the algorithm
    - The hash function 𝐻H
    - the public key 𝑦y
3. **Signing:**
    
    - The signer can now sign a message 𝑚m. The resulting signature is (𝑟,𝑠)(r,s)
    - The message and signature are both now sent to the recipient
	![[Pasted image 20240701115822.png|500]]

4. **Verification:**

The recipient now wishes to verify the authenticity of the sender. They have access to the **public information (𝑞,𝑝,𝑔,𝐻,𝑦,(𝑟,𝑠),𝑚)** They can execute a calculation which proves that the sender had access to the private key 𝑥 and seeks to ascertain that the signer is someone with access to the private key 𝑥.
![[Pasted image 20240701121029.png|500]]


```
Digital Signature Algorithm (DSA)
├── Introduction
│   ├── Digital Signature
│   │   ├── Data Integrity
│   │   ├── Authentication
│   │   └── Non-repudiation
│   └── Asymmetric Cryptography
│       ├── Public Key
│       └── Private Key
├── Key Generation
│   ├── Choose Prime Numbers (p, q)
│   ├── Compute Generator (g)
│   ├── Choose Private Key (x)
│   └── Compute Public Key (y)
├── Signing Process
│   ├── Hash the Message (m)
│   ├── Generate Random Number (k)
│   ├── Compute r and s
│   │   ├── r = (g^k mod p) mod q
│   │   └── s = (k^-1 * (H(m) + x*r)) mod q
│   └── Digital Signature (r, s)
└── Verification Process
    ├── Compute w = s^-1 mod q
    ├── Compute u1 = H(m) * w mod q
    ├── Compute u2 = r * w mod q
    ├── Compute v = ((g^u1 * y^u2) mod p) mod q
    └── If v == r, the signature is valid
```

