Cryptography Fundamentals – Apex Planet Internship

1. Introduction to Cryptography

Cryptography is the technique of protecting information by converting readable data into an encoded form so that unauthorized users cannot understand it.

It is widely used in cybersecurity to protect passwords, financial transactions, communications, and sensitive information.

2. Types of Cryptography

2.1 Symmetric Encryption

Symmetric encryption uses the same secret key for both encryption and decryption.

Example algorithms:

- AES (Advanced Encryption Standard)
- 3DES (Triple Data Encryption Standard – legacy)

Advantages:

- Fast encryption and decryption.
- Suitable for large amounts of data.

Limitation:

- The secret key must be shared securely.

2.2 Asymmetric Encryption

Asymmetric encryption uses two related keys:

- Public Key: Can be shared with others.
- Private Key: Must be kept secret.

Example algorithms:

- RSA
- ECC (Elliptic Curve Cryptography)

Advantages:

- Supports secure key exchange and digital signatures.
- Does not require sharing the private key.

3. Hashing

Hashing converts input data into a fixed-length output called a hash value.

Important characteristics:

- One-way operation.
- Small changes in input produce different hash values.
- Used for integrity verification.

Common algorithms:

Algorithm| Description
MD5| Produces a 128-bit hash; considered cryptographically broken.
SHA-1| Produces a 160-bit hash; no longer recommended for security.
SHA-256| Produces a 256-bit hash and is widely used.
SHA-512| Produces a 512-bit hash.

Note: Hashing is not encryption because it is not designed to be reversed.

4. Digital Certificates

A digital certificate is an electronic document used to associate a public key with an identity.

It is commonly issued and digitally signed by a Certificate Authority (CA).

Digital certificates help establish trust in HTTPS connections.

5. SSL and TLS

SSL and TLS are cryptographic protocols used to protect communication over networks.

- SSL is outdated and insecure.
- TLS is the modern protocol used to secure network communication.
- HTTPS uses TLS to protect web traffic.

TLS provides:

- Confidentiality
- Integrity
- Authentication

6. Practical Activity 1 – Generate a SHA-256 Hash

Command:

echo "Apex Planet Internship" | sha256sum

This command generates a SHA-256 hash of the given text.

7. Practical Activity 2 – Create an Encrypted File Using OpenSSL

Step 1: Create a text file

echo "Cybersecurity Internship Practical" > message.txt

Step 2: Encrypt the file

openssl enc -aes-256-cbc -salt -pbkdf2 -in message.txt -out encrypted.txt

Enter and remember a password when prompted.

Step 3: Decrypt the file

openssl enc -aes-256-cbc -d -pbkdf2 -in encrypted.txt -out decrypted.txt

Enter the same password.

Step 4: Verify the decrypted content

cat decrypted.txt

The original text should appear.

Step 5: Compare SHA-256 hashes

sha256sum message.txt decrypted.txt

Both files should have matching hashes if the decrypted content is identical.

8. Difference Between Encryption and Hashing

Encryption| Hashing
Protects data confidentiality.| Helps verify data integrity.
Can be reversed using the correct key.| Designed to be one-way.
Uses encryption and decryption keys.| Produces a hash value.
Example: AES| Example: SHA-256

9. Applications of Cryptography

1. Secure online banking.
2. Password and data protection.
3. Secure website communication.
4. Digital signatures.
5. Secure file storage.
6. Data integrity verification.

10. Conclusion

Cryptography is an important part of cybersecurity. Understanding symmetric encryption, asymmetric encryption, hashing, digital certificates, and TLS helps protect sensitive information and secure digital communication.
