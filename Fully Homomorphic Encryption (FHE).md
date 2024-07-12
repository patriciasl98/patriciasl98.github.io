---
tags:
  - Concept
  - criptografía
Sumary: is a type of encryption that allows computations to be performed on encrypted data without decrypting it first
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

**Fully Homomorphic Encryption (FHE) is a type of encryption that allows computations to be performed on encrypted data without decrypting it first. This means that sensitive data can be processed and analyzeg it in plaintext, ensuring the confidentiality and integrity of the data.**

In traditional encryption schemes, data is encrypted, transmitted, and then decrypted before it can be processed. However, with FHE, the encrypted data can be directly operated on, and the result will still be encrypted. This allows for secure outsourcing of computations, such as cloud computing, and enables secure data sharing and collaboration.

FHE schemes typically consist of three components:

1. **Key generation**: A pair of keys is generated, a public key and a private key.
2. **Encryption**: The plaintext data is encrypted using the public key.
3. **Evaluation**: The encrypted data is operated on using homomorphic operations (e.g., addition, multiplication).

The properties of FHE schemes include:

1. **Homomorphism**: The scheme allows for homomorphic operations (e.g., addition, multiplication) on encrypted data.
2. **Semantic security**: The scheme ensures that the encrypted data remains confidential, even if an attacker has access to the ciphertext.
3. **Compactness**: The scheme ensures that the ciphertext is compact and doet grow exponentially with the number of operations.

Applications of FHE include:

1. **Secure cloud computing**: FHE enables secure outsourcing of computations to the cloud, ensuring that data remains confidential.
2. **Private data sharing**: FHE allows for securf sensitive data between organizations or individuals.
3. **Secure machine learning**: FHE enables machine learning models to be trained on encrypted data, ensuring the confidentiality of the data.

While FHE is a powerful tool for securing data, it is still a developing field, and there are challenges to be addressed, such as:

1. **Efficiency**: FHE schemes are often computationally expensive, which can limit their practical adoption.
2. **Scalability**: FHE schemes need to be scalable to handle large datasets and complex computations.
3. **Standardization**: There is a need for standardization of FHE schemes to ensure interoperability and widespread adoption.

