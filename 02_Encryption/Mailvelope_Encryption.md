# Mailvelope Encryption Walkthrough

[← Back to index](../README.md)

Mailvelope is a browser extension that adds **PGP** (asymmetric) encryption to webmail.

## Steps
1. Install the Mailvelope browser extension.
2. Generate a key pair (public + private) and set a strong passphrase.
3. Export and share only the **public key**; never share the private key.
4. Import the recipient's public key.
5. Compose a message and encrypt it with the recipient's public key.
6. The recipient decrypts it with their private key and passphrase.

## Concept link
Applies [asymmetric encryption](Encryption_Fundamentals.md): public key encrypts, private key decrypts. Signing uses the reverse for authenticity.

## Key management reminders
- Protect the private key and passphrase; never share them.
- Share only the public key.
- Verify that you are encrypting with the recipient's public key.

## My Reflection
I learned about the importance of encrypting email messages to protect sensitive information from unauthorized access. The activity introduced me to public-key and private-key concepts and how encryption can help secure communication. I also understood that private keys must be protected and should never be shared with other people. This lesson showed me how encryption can improve privacy when sending confidential messages online.

## Review Questions
1. Which key is shared publicly?
2. What happens if the private key is lost?
3. What does the passphrase protect?
