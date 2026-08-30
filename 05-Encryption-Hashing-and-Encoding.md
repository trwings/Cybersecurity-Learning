# Encryption, Hashing and Encoding

## 1. Introduction

Encryption, hashing, and encoding are frequently confused because all three can transform data.

However, they have different purposes.

The most important distinction is:

```text
Encryption → Protect confidentiality
Hashing    → Produce a one-way representation
Encoding   → Represent data in another format
```

---

# 2. Encryption

Encryption is the process of transforming readable data, called **plaintext**, into an unreadable form called **ciphertext** using an algorithm and key.

Basic model:

```text
Plaintext
    +
Encryption Algorithm
    +
Key
    ↓
Ciphertext
```

The intended recipient can use the appropriate key to recover the plaintext.

---

# 3. Decryption

Decryption converts ciphertext back into plaintext.

```text
Ciphertext
    +
Decryption Algorithm
    +
Key
    ↓
Plaintext
```

---

# 4. Why Encryption is Used

Encryption can help protect confidentiality.

Examples:

* HTTPS
* Encrypted storage
* VPNs
* Encrypted messaging
* Disk encryption

---

# 5. Symmetric Encryption

In symmetric encryption, the same secret key is used for encryption and decryption.

```text
         Same Secret Key
              ↓
Plaintext → Encryption → Ciphertext
                           ↓
                       Decryption
                           ↓
                        Plaintext
```

Advantages:

* Fast
* Efficient for large amounts of data

Challenge:

> How can the communicating parties securely share the secret key?

Examples include:

* AES
* ChaCha20

---

# 6. Asymmetric Encryption

Asymmetric cryptography uses a key pair:

* Public key
* Private key

The public key can generally be shared.

The private key must be protected.

Basic concept:

```text
Public Key
    ↓
Encryption
    ↓
Ciphertext
    ↓
Private Key
    ↓
Decryption
```

Asymmetric cryptography is generally slower than symmetric encryption.

It is commonly used for:

* Secure key exchange
* Digital signatures
* Authentication
* Public-key infrastructure

Examples:

* RSA
* Elliptic Curve Cryptography (ECC)

---

# 7. Public Key vs Private Key

### Public Key

Can be shared.

### Private Key

Must remain secret.

Never treat a private key like a public identifier.

---

# 8. Digital Signatures

Digital signatures provide mechanisms for verifying:

* Authenticity
* Integrity

They can also support non-repudiation depending on the system and legal context.

Simplified process:

```text
Message
   ↓
Hash
   ↓
Digital Signature using private key
   ↓
Signature
```

The recipient can use the corresponding public key to verify the signature.

---

# 9. Hashing

Hashing is the process of converting input data into a fixed-length output called a hash or digest.

Example:

```text
Input
  ↓
Hash Function
  ↓
Digest
```

A cryptographic hash function is designed so that it is computationally difficult to recover the original input from the hash.

---

# 10. Important Properties of Cryptographic Hashes

A good cryptographic hash function aims to provide properties such as:

### Deterministic

The same input produces the same output.

### One-way

It should be computationally infeasible to reverse the hash to recover the original input.

### Collision Resistance

It should be computationally difficult to find two different inputs producing the same hash.

### Avalanche Effect

A small change in input should produce a substantially different digest.

---

# 11. Common Hash Functions

Examples:

* SHA-256
* SHA-512
* SHA-3

Older algorithms such as MD5 and SHA-1 are not suitable for many modern security applications because of known collision weaknesses.

---

# 12. Password Hashing

Passwords should not normally be encrypted for storage merely because they need to be "protected."

Instead, password storage should use dedicated password-hashing approaches.

Common password-hashing algorithms include:

* Argon2
* bcrypt
* scrypt

A password system should also use salts.

---

# 13. What is a Salt?

A salt is additional random data combined with a password before password hashing.

Conceptually:

```text
Password + Unique Salt
          ↓
    Password Hash
```

A unique salt helps prevent attackers from efficiently using precomputed tables against many password hashes.

---

# 14. Encryption vs Hashing

| Encryption                          | Hashing                                                                                     |
| ----------------------------------- | ------------------------------------------------------------------------------------------- |
| Designed to protect confidentiality | Designed to produce a digest                                                                |
| Uses keys                           | Cryptographic hash functions do not use an encryption key in the normal sense               |
| Reversible with appropriate key     | Designed to be one-way                                                                      |
| Plaintext → ciphertext              | Input → digest                                                                              |
| Used for confidential data          | Used for integrity checks and password storage with appropriate password-hashing algorithms |

---

# 15. Encoding

Encoding converts data into another representation according to a defined format.

It is **not encryption**.

The purpose is usually compatibility, transport, storage, or representation.

Examples:

* Base64
* URL encoding
* Unicode encodings

---

# 16. Base64

Base64 converts binary data into a text representation using a defined character set.

For example:

```text
Hello
```

can be represented as:

```text
SGVsbG8=
```

This does NOT mean the data is encrypted.

Anyone who knows the encoding can decode it.

---

# 17. Encoding vs Encryption

### Encoding

Purpose:

> Data representation.

Does not provide confidentiality.

### Encryption

Purpose:

> Confidentiality.

Requires cryptographic protection and appropriate keys.

---

# 18. Encoding vs Hashing

### Encoding

Usually reversible.

```text
Data
 ↓
Encode
 ↓
Encoded data
 ↓
Decode
 ↓
Original data
```

### Hashing

Designed to be one-way.

```text
Data
 ↓
Hash
 ↓
Digest
```

---

# 19. Comparison Table

| Property     | Encryption                | Hashing                                             | Encoding               |
| ------------ | ------------------------- | --------------------------------------------------- | ---------------------- |
| Main purpose | Confidentiality           | Digest/integrity/password protection                | Representation         |
| Reversible?  | Yes, with appropriate key | Designed to be one-way                              | Usually yes            |
| Uses key?    | Yes                       | No encryption key in standard cryptographic hashing | No                     |
| Output       | Ciphertext                | Hash/digest                                         | Encoded representation |
| Example      | AES                       | SHA-256                                             | Base64                 |
| Secret?      | Key must be protected     | Hash may be stored depending on use                 | No secret required     |
| Typical use  | Protect data              | Integrity/password storage                          | Data transport/format  |

---

# 20. Example

Suppose we have:

```text
Password123
```

### Encoding

Could produce a Base64 representation.

This is not secure password protection.

### Encryption

The data can be encrypted using an appropriate algorithm and key.

### Password Hashing

A password-hashing algorithm such as Argon2 can produce a password hash suitable for verification.

These three operations solve different problems.

---

# 21. HTTPS

HTTPS uses cryptographic protocols to protect web communication.

It provides important security properties such as:

* Confidentiality
* Integrity
* Authentication of the server through certificates

HTTPS is built on TLS.

Basic concept:

```text
Browser
   ↓
TLS-secured connection
   ↓
Web Server
```

---

# 22. TLS

**Transport Layer Security (TLS)** is a cryptographic protocol used to secure communications over networks.

TLS can provide:

* Encryption
* Integrity protection
* Server authentication

TLS is used by HTTPS.

---

# 23. Certificates

Digital certificates are used in systems such as HTTPS to bind identities to public keys.

A browser can validate information in a server certificate through the certificate trust model.

---

# 24. Common Mistakes

### Mistake 1

"Base64 is encryption."

False.

Base64 is encoding.

### Mistake 2

"Hashing and encryption are the same."

False.

Hashing is designed as a one-way transformation; encryption is designed to be reversible with the appropriate key.

### Mistake 3

"All hashes are good for passwords."

False.

General-purpose hashes such as SHA-256 are not password-hashing algorithms by themselves.

Dedicated password-hashing algorithms should be used.

---

# 25. Memory Trick

Remember:

```text
Encryption = Lock the data

Hashing = Fingerprint the data

Encoding = Change the representation
```

---

## Key Terms

```text
Plaintext
Ciphertext
Encryption
Decryption
Symmetric Encryption
Asymmetric Cryptography
Public Key
Private Key
Digital Signature
Hash
Digest
SHA-256
SHA-512
SHA-3
Salt
Password Hashing
Argon2
bcrypt
scrypt
Encoding
Base64
TLS
HTTPS
Digital Certificate
```
