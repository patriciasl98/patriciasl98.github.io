---
tags:
  - Concept
  - criptografía
Sumary: Cryptographic protocol designed to provide secure communication over a computer network.
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
**Transport Layer Security (TLS)** is a cryptographic protocol designed to provide secure communication over a computer network. It is the successor to the **Secure Sockets Layer (SSL)** protocol and is widely used to secure **internet communications**, such as web browsing, email, instant messaging, and voice over IP (VoIP).

Transport Layer Security (TLS) is a cryptographic protocol designed to provide secure communication over a computer network. It is widely used to secure web traffic, emails, instant messaging, and other types of data exchanges. Here’s an overview of its key features, components, and functions:

### Key Features of TLS
1. **Encryption**: Ensures that the data transmitted between parties is unreadable by anyone else.
2. **Integrity**: Protects data from being altered during transmission.
3. **Authentication**: Verifies the identities of the communicating parties.

### Components of TLS
1. **TLS Handshake Protocol**: Establishes the parameters of the secure session.
2. **TLS Record Protocol**: Manages the secured data transmission.
3. **Alert Protocol**: Communicates any errors in the connection.
4. **Change Cipher Spec Protocol**: Signals changes in the encryption parameters.

### TLS Handshake Process
1. **Client Hello**: The client initiates the handshake by sending a “Client Hello” message to the server, which includes information like the TLS version, cipher suites supported, and a randomly generated number.
2. **Server Hello**: The server responds with a “Server Hello” message that includes the chosen cipher suite, TLS version, and another random number.
3. **Server Certificate**: The server sends its digital certificate to the client for authentication.
4. **Server Key Exchange (optional)**: If the server requires a key exchange, it sends a key exchange message.
5. **Client Key Exchange**: The client responds with a key exchange message.
6. **Change Cipher Spec**: Both the client and server send a “Change Cipher Spec” message to indicate that subsequent messages will be encrypted.
7. **Finished**: Both parties send a “Finished” message encrypted with the agreed-upon session keys, completing the handshake.

### Encryption in TLS
- **Symmetric Encryption**: Used for the actual data transmission because it is fast. Both parties use the same key for encryption and decryption.
- **Asymmetric Encryption**: Used during the handshake to securely exchange the keys. It involves a public key and a private key.
- **Hash Functions**: Ensure data integrity by creating a unique fingerprint of the data.

### TLS Versions
- **TLS 1.0**: The first version, now considered obsolete.
- **TLS 1.1**: Introduced improved security features but also largely obsolete.
- **TLS 1.2**: Widely used, with stronger security measures and improved performance.
- **TLS 1.3**: The latest version, offering faster handshakes and even stronger security features.

### Security Improvements in TLS 1.3
- **Faster Handshake**: Reduced from two round trips to one, improving performance.
- **Simplified Cipher Suites**: Removal of weak and obsolete algorithms.
- **Forward Secrecy**: Ensures session keys are not compromised even if the private key is.

### Applications of TLS
- **HTTPS**: Secures web traffic.
- **Email**: Protects email communications through protocols like SMTPS, IMAPS, and POP3S.
- **VPNs**: Ensures secure remote connections.
- **Instant Messaging**: Encrypts messages in transit.

### Conclusion
TLS is essential for maintaining privacy and security in digital communications. By encrypting data, authenticating parties, and ensuring data integrity, TLS provides a robust framework for secure communication over the internet and other networks.