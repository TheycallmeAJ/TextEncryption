# TextEncryption
A cybersecurity project that encrypts text using different algorithms like AES, DES, and RSA for secure data protection.

This code is written in Python and uses several modules from the cryptography library to demonstrate symmetric and asymmetric encryption.

First, it imports the necessary modules and classes:

Fernet from cryptography.fernet is used for AES (Advanced Encryption Standard) symmetric encryption.
hashes, padding, serialization, rsa from cryptography.hazmat.primitives are used for various cryptographic functions.
generate_private_key and public_key from cryptography.hazmat.primitives.asymmetric.rsa are used to generate RSA key pairs.
The code defines two functions:

aes_encryption(message, key): This function takes a message and an AES key as input. It creates a Fernet object using the key, then uses it to encrypt the message. The encrypted message is returned.
rsa_encryption(message, public_key): This function takes a message and an RSA public key as input. It loads the public key, then uses it to encrypt the message with OAEP (Optimal Asymmetric Encryption Padding) and the SHA-256 hash algorithm. The encrypted message is returned.
Next, the code generates a key for AES encryption using Fernet.generate_key() and assigns it to the variable key. It also generates a key pair for RSA encryption using rsa.generate_private_key() and assigns the private key to private_key and the public key to public_key. The public key is then serialized as a PEM-encoded SubjectPublicKeyInfo object and saved to the variable pem.

A test message is defined as message = b"A really secret message, maybe a pincode".

The code then performs AES and RSA encryption on the test message using the generated keys and prints the encrypted messages:

AES Encrypted message: <encrypted message>
RSA Encrypted message: <encrypted message>
Remember, the actual encrypted messages will differ each time the code runs due to the random nature of encryption.
