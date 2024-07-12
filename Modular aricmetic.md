---
dg-publish: true
tags:
  - Concept
  - maths
Sumary: Concepto matemático de aritmética modular y inverso multiplicativo
---
```dataview
TABLE WITHOUT ID link(file.name) AS "Nota", file.cday AS "Created date" 
FROM ""
WHERE contains(file.outlinks, this.file.link)
OR contains(file.inlinks, this.file.link)
AND file.name != this.file.name
```


La aritmética modular es un sistema matemático que se ocupa d**e números enteros y se basa en la idea de congruencia**. En aritmética modular, dos números son considerados **congruentes si al dividirlos por un número entero positivo llamado módulo, ambos números tienen el mismo residuo.** La congruencia se denota generalmente como **"a ≡ b (mod m)"**, donde "a" y "b" son los números enteros y "m" es el módulo.

Un ejemplo simple de aritmética modular es el sistema de horas en un reloj. En un reloj de 12 horas, después de las 12:00 PM, las horas se reinician desde la 1:00 PM. Entonces, si son las 10:00 AM y queremos saber qué hora será en 5 horas, sumamos 10+5=15. En un reloj de 12 horas, esto correspondería a las 3:00 PM. En aritmética modular, esto se expresa como 10+5 ≡ 3 (mod 12).

Ejmplos: 
10 ≡ 3 (mod 7).
17 ≡ 3 (mod 7).

La aritmética modular se utiliza en muchos campos de la matemática y ciencias de la computación, incluyendo la criptografía, la teoría de números y la resolución de sistemas de ecuaciones lineales.

---

# Mind MAP
Sure, I can create a mind map that connects the concepts explained in modular arithmetic and its uses for cryptography. A mind map is a visual representation that helps organize and understand information in a hierarchical and interconnected manner. Here's a mind map that covers the key concepts:

```
Modular Arithmetic and Cryptography
├── Modular Arithmetic
│   ├── Congruence
│   │   ├── Definition: a ≡ b (mod n) if a and b have the same remainder when divided by n
│   │   └── Properties
│   │       ├── Reflexive: a ≡ a (mod n)
│   │       ├── Symmetric: If a ≡ b (mod n), then b ≡ a (mod n)
│   │       └── Transitive: If a ≡ b (mod n) and b ≡ c (mod n), then a ≡ c (mod n)
│   ├── Modular Arithmetic Operations
│   │   ├── Addition: (a + b) mod n
│   │   ├── Subtraction: (a - b) mod n
│   │   ├── Multiplication: (a × b) mod n
│   │   └── Exponentiation: (a^b) mod n
│   └── Modular Inverse
│       ├── Definition: a^(-1) (mod n) such that (a × a^(-1)) ≡ 1 (mod n)
│       └── Applications
│           ├── Solving linear congruences
│           └── Cryptography (e.g., RSA)
├── Cryptography
│   ├── Symmetric-key Cryptography
│   │   ├── Definition: Same key used for encryption and decryption
│   │   └── Examples: AES, DES
│   └── Asymmetric (Public-key) Cryptography
│       ├── Definition: Different keys for encryption and decryption
│       ├── RSA Cryptosystem
│       │   ├── Key Generation
│       │   │   ├── Choose two large prime numbers (p, q)
│       │   │   ├── Compute n = p × q
│       │   │   ├── Choose public exponent e (coprime to (p-1)(q-1))
│       │   │   ├── Compute private exponent d = e^(-1) (mod (p-1)(q-1))
│       │   │   └── Public Key: (e, n), Private Key: (d, n)
│       │   ├── Encryption: c = m^e (mod n)
│       │   └── Decryption: m = c^d (mod n)
│       └── Applications
│           ├── Secure communication
│           ├── Digital signatures
│           └── Key exchange protocols
```

# Examples: 


1. **Diffie-Hellman Key Exchange:**
   Suppose Alice and Bob want to establish a shared secret key over an insecure communication channel, such as the internet. They can use the Diffie-Hellman key exchange protocol, which relies on modular arithmetic operations.

   Let's assume they agree on a public modulus **p = 23 and a base g = 5.**

   **Alice** chooses a secret number **a = 6,** and computes **A = (g^a) mod p** = (5^6) mod 23 = 8.
   **Bob** chooses a secret number **b = 3,** and computes **B = (g^b) mod p** = (5^3) mod 23 = 10.

   **Alice sends A (8) to Bob, and Bob sends B (10) to Alice**.

   Alice computes the **shared secret key K = (B^a) mod p = (10^6) mod 23 = 18.**
   Bob computes the **shared secret key K = (A^b) mod p = (8^3) mod 23 = 18.**

   Now, Alice and Bob have established a shared secret key (18) without ever exchanging their private values (a and b) over the insecure channel.

2. RSA Encryption and Decryption:

   The RSA cryptosystem is widely used for secure data transmission and relies heavily on modular arithmetic operations.
   Suppose Alice wants to send a confidential message to Bob using RSA encryption.

   Bob generates a public key (e, n) and a private key (d, n), where n is the modulus, e is the public exponent, and d is the private exponent.

   Let's assume Bob's public key is (e = 5, n = 77) and his private key is (d = 29, n = 77).

   Alice converts her message into a numerical value M = 35 and encrypts it using Bob's public key: C = (M^e) mod n = (35^5) mod 77 = 63.

   Alice sends the ciphertext C (63) to Bob.

   Bob decrypts the ciphertext using his private key: M = (C^d) mod n = (63^29) mod 77 = 35.

   Bob recovers the original message M (35) from Alice.

3. Elliptic Curve Cryptography (ECC):

   ECC is another widely used public-key cryptography system that **relies on modular arithmetic operations on elliptic curves over finite fields.**
   Suppose Alice and Bob want to establish a shared secret key using ECC over a finite field modulo p = 17.

   They agree on an elliptic curve equation y^2 = x^3 + x + 1 (mod 17) and a base point G = (3, 10) on the curve.

   Alice chooses a secret number a = 5 and computes her public key A = a × G = (5, 8).
   Bob chooses a secret number b = 7 and computes his public key B = b × G = (6, 13).

   Alice computes the shared secret key K = a × B = (5 × (6, 13)) = (16, 7).
   Bob computes the shared secret key K = b × A = (7 × (5, 8)) = (16, 7).

   Now, Alice and Bob have established a shared secret key (16, 7) using modular arithmetic operations on the elliptic curve.


----

# multiplicative inverses

Inverso Multiplicativo

A. Definición

- El inverso multiplicativo de un número **a módulo n es un número b tal que (a * b) mod n = 1.**
- Se denota como: **a^(-1) mod n**

B. Propiedades

- Un inverso multiplicativo existe solo si a y n son coprimos (su máximo común divisor es 1).
- El inverso multiplicativo se utiliza en operaciones de aritmética modular, como la división modular.

C. Aplicaciones

- Los inversos multiplicativos se utilizan en esquemas de firmas digitales, como el Algoritmo de Firma Digital (DSA) y el Algoritmo de Firma Digital de Curva Elíptica (ECDSA).
- Se usan en los procesos de generación y verificación de firmas para asegurar la autenticidad e integridad de los datos firmados.

D. Ejemplo

### Ejemplo de Inverso Multiplicativo

Supongamos que queremos encontrar el **inverso multiplicativo de \( 3 \) módulo \( 11 \).**

La definición dice que el inverso multiplicativo de un número **\( a \) módulo \( n \) es un número \( b \) tal que:**

**\[ (a \times b) \mod n = 1 \]**

Entonces, en este caso, buscamos un número \( b \) tal que:

\[ (3 \times b) \mod 11 = 1 \]

Para encontrar el valor de \( b \), probamos varios valores hasta encontrar uno que satisfaga la condición:
>[!Nota]
>El cálculo de 3mod  11 ->  implica encontrar el resto de la división de 3 por 11. En este caso
>1. Dividimos 3 entre 11.
>2. El cociente es 0 porque 3 es menor que 11.
>3. El residuo es 3 porque no podemos dividir 3 entre 11 completamente.
>Por lo tanto: 3 mod  11=3

- \( b = 1 \): \( (3 \times 1) \mod 11 = 3 \mod 11 = 3 \) (no es igual a 1)
- \( b = 2 \): \( (3 \times 2) \mod 11 = 6 \mod 11 = 6 \) (no es igual a 1)
- \( b = 3 \): \( (3 \times 3) \mod 11 = 9 \mod 11 = 9 \) (no es igual a 1)
- \( b = 4 \): \( (3 \times 4) \mod 11 = 12 \mod 11 = 1 \) (¡este sí es igual a 1!)

Entonces, el inverso multiplicativo de \( 3 \) módulo \( 11 \) es \( 4 \), porque:

\[ (3 \times 4) \mod 11 = 12 \mod 11 = 1 \]
