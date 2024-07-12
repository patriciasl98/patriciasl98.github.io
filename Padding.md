---
tags:
  - Concept
  - criptografía
Sumary: Padding is a technique used to ensure that data conforms to a certain block size required by the encryption algorithm
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

Padding is a technique used to ensure that data conforms to a certain block size required by the encryption algorithm. Since many cryptographic algorithms operate on fixed-size blocks of data, padding is necessary when the data does not perfectly fit into these blocks. Here's a breakdown to help you understand the text:

### Padding in Cryptography

1. **Block Ciphers and Padding:**
   - **Block Ciphers**: These algorithms encrypt data in fixed-size blocks (e.g., 128 bits for AES). If the data isn't a multiple of the block size, padding is used to fill the last block.
   - **Padding Methods**: Common padding schemes include PKCS#7, which adds bytes to the end of the data, each byte representing the number of padding bytes added.

2. **Semantic Security:**
   - **Definition**: Semantic security ensures that an attacker cannot derive any meaningful information from the ciphertext. It means that identical plaintexts encrypted under the same key will produce different ciphertexts.
   - **Importance**: Without semantic security, patterns in the encrypted data could reveal information about the original plaintext.

### OAEP (Optimal Asymmetric Encryption Padding)

1. **Purpose of OAEP:**
   - OAEP is a padding scheme specifically designed for use with RSA encryption.
   - It enhances the security of RSA by adding randomness to the plaintext before encryption, making it semantically secure.

2. **How OAEP Works:**
   - **Random Padding**: OAEP combines the plaintext with a random padding string, ensuring that the same plaintext will encrypt to different ciphertexts each time.
   - **Hash Functions**: It uses hash functions to mix the plaintext and padding, ensuring that small changes in the plaintext or padding result in significant changes in the ciphertext.

3. **Ensuring Semantic Security:**
   - **Randomization**: The inclusion of randomness means that even if the same message is encrypted multiple times, the resulting ciphertexts will be different.
   - **Protection**: This prevents attackers from gaining information by comparing ciphertexts, thus ensuring semantic security.

### Example Scenario

Imagine Alice wants to send a secure message to Bob. Without padding like OAEP, if Alice sends the same message multiple times, an attacker intercepting the messages could notice that the ciphertexts are identical, revealing that the same plaintext was sent each time. By using OAEP, each encryption of the same message will result in different ciphertexts, preventing the attacker from making such deductions.
