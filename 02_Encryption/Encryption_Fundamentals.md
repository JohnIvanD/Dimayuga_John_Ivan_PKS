# Encryption Fundamentals

[← Back to index](../README.md)

**Encryption** converts plaintext into ciphertext using an algorithm and a key. **Decryption** reverses it with the correct key.

## Symmetric vs asymmetric
| | Symmetric | Asymmetric |
|---|---|---|
| Keys | One shared secret key | Public key and private key |
| Speed | Fast | Slower |
| Examples | AES | RSA, ECC |
| Challenge | Securely sharing the key | Computational cost |
| Best for | Encrypting large data | Key exchange, signatures |

## Hashing
- One-way function: cannot be reversed.
- Used for password storage and integrity checks (e.g., SHA-256).
- MD5 and SHA-1 are considered weak.
- Hashing is not encryption: there is no key to decrypt.

## Digital signatures
Signed with the **private key**, verified with the **public key**. Provides integrity, authenticity, and non-repudiation.

## Hybrid encryption (HTTPS/TLS)
Asymmetric crypto exchanges a session key, then symmetric crypto protects the data.

## My Reflection
I learned how encryption helps protect sensitive information by converting readable data into a form that unauthorized people cannot easily understand. I also learned the difference between public and private keys and how they are used in cryptography. The Mailvelope activity helped connect these concepts to email security. This lesson showed me that encryption is important when transmitting confidential information and protecting personal data.

## Review Questions
1. Why is hashing not encryption?
2. Which key encrypts a message to Maria: yours, her public key, or her private key?
3. Why do real systems combine symmetric and asymmetric encryption?
