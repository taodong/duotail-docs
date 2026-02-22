---
sidebar_label: Message Storage Security
sidebar_position: 2
---

# Message Storage Security

All messaged stored on our server are encrypted by a public key generated through user provided key words. We aren't able to read the content because we store neither the key words nor the private key.


1. Customer provides three words and a key name
2. Our system uses the three words to generate a encrypt key under the key name
3. Our system stores the encrypt key and key name in our database
3. When saving messages to file, system encrypts the content using the encrypt key
4. When customer downloads the file, our system asks the three words under the key name
5. Our system uses the three words to generate a decrypt key
6. Our system decrypts the file using the decrypt key and sends the original file to the customer end

Details

![Encryption/Decryption Flow](/img/privacy/encryption-flow.png)