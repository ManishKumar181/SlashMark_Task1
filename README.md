# SlashMark_Task1
Text Encryption Using Cryptographic Algorithms.

This repository provides a simple JAVA script to read lines from a text file, encrypt each line using cryptographic algorithms encryption, and write the encrypted lines to a new file.
This code defines two functions, encrypt and decrypt, using the Node.js crypto module to perform AES-256-CBC encryption and decryption. Here is a breakdown of what the code does:

# Strict Mode:
The code starts with 'use strict'; to enforce strict mode, which helps catch common coding mistakes and unsafe actions. Require Crypto Module: The crypto module is required to perform cryptographic operations.

# Encryption Key and IV Length:
ENCRYPTION_KEY is expected to be a 256-bit (32-character) key retrieved from the environment variable process.env.ENCRYPTION_KEY. IV_LENGTH is set to 16, which is the required length for the Initialization Vector (IV) in AES.

# Encrypt Function:
Generates a random IV of 16 bytes. Creates a cipher using the AES-256-CBC algorithm with the encryption key and IV. Encrypts the given text and concatenates the result with the final encrypted block. Returns the IV and encrypted text as a single string, separated by a colon, in hexadecimal format.

# Decrypt Function:
Splits the input text into IV and encrypted text parts. Converts these parts from hexadecimal to binary buffers. Creates a decipher using the AES-256-CBC algorithm with the encryption key and IV. Decrypts the encrypted text and concatenates the result with the final decrypted block. Returns the decrypted text as a string. Export Functions: Both encrypt and decrypt functions are exported as a module.
