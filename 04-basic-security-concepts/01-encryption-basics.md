# Encryption Basics
Encryption is about protecting data by converting into cipher code so only authorized people can decrypt and read it.

### Type of Encryption
- 1. Symmetric Encryption
  - Same key is used to encrypt and decrypt data.
  - Fast, but both sender and receiver must share the key safely.
  - Example Algorithms: AES, DES
  
- 2. Asymmetric Encryption
  - Uses a pair of keys: public key (to encrypt) and private key (to decrypt)
  - More secure for communication, but slower.
  - Example Algorithms: RSA, ECC

### Hashing
Turns data into fixed lenght as unique string. Its one way and can't get the original data back. Used to store passwords or verify data. Examples: MD5 (insecure), SHA-1 (weak), SHA-256 (secure).

### Digital Signatures
Proves that a message or document is authentic and hasn't been changed. It is combination of hashing and asymmetric encryption. Used in software, emails, and legal documents.

### Certificates & PKI
PKI (Public Key Infrastructure) is the system that manages encryption keys and certificates. Certificates are like digital IDs that prove ownership of a public key. Issued by companies called Certificate Authorities(CA).