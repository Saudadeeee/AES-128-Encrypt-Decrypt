# AES-128 Encryption/Decryption Tool

This tool implements AES-128 encryption and decryption in C++. It provides a command-line interface to encrypt a normal string message and save it to a file, and to decrypt the message from that file back to a normal string.

## Features

- **Encrypt** a normal string message and save it in hexadecimal format to `message.aes`.
- **Decrypt** a message from the `message.aes` file back to a normal string.

## Prerequisites

- C++ compiler (e.g., g++, clang++)
- Basic understanding of AES encryption and decryption

## Usage

1. **Compile the Program**

   Ensure you have a C++ compiler installed. Compile the source code with:

   ```bash
   g++ -o aes_tool aes_tool.cpp
Run the Program

Run the compiled program:

bash
Sao chép mã
./aes_tool
You will be prompted to choose between encryption and decryption.

Encryption

Select option 1 to encrypt a message.
Enter the message you want to encrypt.
The encrypted message will be saved to message.aes and displayed in hexadecimal format.
Decryption

Select option 2 to decrypt a message.
The program will read from message.aes, decrypt the message, and display the result.
Key
The AES-128 algorithm requires a 16-byte key. Modify the key array in the source code to use your desired key.

cpp
Sao chép mã
unsigned char key[16] = { /* 16 bytes key here */ };
Padding
The program uses PKCS7 padding to ensure the input string fits the 16-byte block size required by AES. The padding is automatically handled during encryption and removed during decryption.

Files
aes_tool.cpp: The main source code file for the AES-128 encryption/decryption tool.
message.aes: The file where the encrypted message is saved.
Example
Encrypt
bash
Sao chép mã
./aes_tool
mathematica
Sao chép mã
AES-128 Encryption/Decryption Tool
1. Encrypt message
2. Decrypt message
Enter option (1 or 2): 1
Enter message (normal string, will be padded to fit 16 bytes): Hello, World!
Encrypted message saved to message.aes
Encrypted message (hex): 7e0a74d62b8a4ed1e482a0b7e4bbf23e
Decrypt
bash
Sao chép mã
./aes_tool
mathematica
Sao chép mã
AES-128 Encryption/Decryption Tool
1. Encrypt message
2. Decrypt message
Enter option (1 or 2): 2
Decrypted message: Hello, World!
