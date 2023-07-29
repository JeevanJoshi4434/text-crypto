
# text-crypto (npm module)

Text-Crypto is a versatile npm module designed to provide robust encryption, hashing, and text comparison functionalities with the added security of salts. This powerful library allows developers to safeguard sensitive data by transforming plain text into encrypted or hashed formats, making it significantly more challenging for unauthorized individuals to access or reverse-engineer the original information.

Key Features:
1. Encryption and Hashing: Text-Crypto offers both encryption and hashing capabilities. Encryption is used to convert plain text into ciphertext, which can later be decrypted back to its original form using a secret key. Hashing, on the other hand, creates a fixed-size string of characters from the input, making it ideal for storing passwords or generating unique identifiers.

2. Salting for Enhanced Security: Salts are random data added to the text before hashing or encryption, providing an additional layer of security against common attacks like rainbow tables or dictionary attacks. By utilizing salts, developers can ensure that even identical pieces of text result in different encrypted or hashed outputs.

3. Secure Text Comparison: Text-Crypto supports secure comparison of encrypted or hashed text. Instead of directly comparing the encrypted or hashed values, this module employs a secure comparison algorithm that mitigates potential timing attacks, providing a safer and more reliable way to check if two pieces of text match.

4. Customizable Options: The module allows developers to customize various aspects of the encryption or hashing process, such as encryption algorithms, hashing algorithms, salt lengths, and more. This flexibility ensures compatibility with specific security requirements and coding preferences.

Sample Usage:

```javascript
const TextCrypto = require('text-crypto');

// Example for Hashing with salt
const textToEncrypt = 'SensitiveData123';
const salt = 10;
const Salt = TextCrypto.getSalt(salt);
const encryptedText = TextCrypto.getString(textToEncrypt, Salt);

// Example for Comparing String with encryptedText

const isMatch = TextCrypto.match(textToEncrypt, encryptedText, salt);

console.log('Hashed Text:', encryptedText);
console.log('Is Match:', isMatch);
```

In summary, Text-Crypto is a reliable npm module that facilitates easy and secure encryption, hashing, and comparison of text, offering developers a valuable tool to protect sensitive data in their applications. Its support for salts ensures a higher level of security against various attacks, making it an essential component in building robust and secure software systems.


## Authors

- [@JeevanJoshi](https://www.github.com/JeevanJoshi4434)

