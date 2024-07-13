# Caesar Cipher Encryption and Decryption

Welcome to the **Caesar Cipher** project! This repository contains a simple implementation of the Caesar Cipher algorithm in Python. The Caesar Cipher is one of the earliest and simplest methods of encryption, named after Julius Caesar, who reportedly used it to communicate securely with his officials.

## Overview

The Caesar Cipher is a substitution cipher where each letter in the plaintext is shifted a certain number of places down or up the alphabet. This project includes two main functions: `encrypt` and `decrypt`, as well as a `main` function to interact with the user.

## Algorithm Explanation

### Encryption

The `encrypt` function takes two parameters: the `text` to be encrypted and the `shift` value, which determines how many places each character in the text is shifted. Here’s how it works:

1. **Initialization**: An empty string `result` is initialized to store the encrypted text.
2. **Iteration**: The function iterates over each character in the input `text`.
3. **Character Check**: For each character, it checks if the character is an alphabet letter using `char.isalpha()`.
4. **Case Check**: It determines whether the character is uppercase or lowercase to handle them separately.
5. **Shift Calculation**: It calculates the new character by shifting the original character by the `shift` value. The calculation involves:
   - Getting the ASCII value of the character using `ord()`.
   - Applying the shift and adjusting for wrap-around within the alphabet using modulo operation.
   - Converting the shifted ASCII value back to a character using `chr()`.
6. **Appending**: The shifted character is appended to the `result` string. Non-alphabet characters are appended without changes.
7. **Return**: The final encrypted string is returned.

### Decryption

The `decrypt` function simply reverses the encryption process. It calls the `encrypt` function with the negative of the `shift` value, effectively reversing the shift applied during encryption.

### Main Function

The `main` function is the entry point of the program. It interacts with the user to get the message and shift value, then displays both the encrypted and decrypted messages.

1. **Input**: Prompts the user to enter the message and shift value.
2. **Encryption**: Calls the `encrypt` function with the user input to get the encrypted message.
3. **Decryption**: Calls the `decrypt` function with the encrypted message to verify the decryption process.
4. **Output**: Prints the encrypted and decrypted messages.

## Usage

To use this program, run the `caesar_cipher.py` script and follow the on-screen instructions to enter your message and shift value. The program will display the encrypted message and then decrypt it back to the original message.

```python
def main():
    message = input("Enter the message: ")
    shift = int(input("Enter the shift value: "))

    encrypted_message = encrypt(message, shift)
    decrypted_message = decrypt(encrypted_message, shift)

    print(f"\nEncrypted message: {encrypted_message}")
    print(f"Decrypted message: {decrypted_message}")

if __name__ == "__main__":
    main()'''''

## Example

Enter the message: Hello World!
Enter the shift value: 3

Encrypted message: Khoor Zruog!
Decrypted message: Hello World!
'''''

##Contributing
Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

###License
This project is licensed under the MIT License. See the LICENSE file for details.

Happy coding! 🚀
