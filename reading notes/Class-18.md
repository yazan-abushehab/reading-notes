# Encryption, Decryption & Hacking
## why this topic matters as it relates to what you are studying in this module ?
A huge amount of private data is sent around the Internet every day: emails with details about our personal lives, passwords that we type into login screens, tax documents that we upload to servers.
The Internet protocols send private data in packets on the same routes as everyone else's data, and unfortunately, attackers have figured out ways to look at the data whizzing around the Internet.

<br>

# Ceasar Cipher
## What is the basic principle behind the Caesar Cipher, and how was it used historically?
The Caesar Cipher is one of the simplest and oldest known substitution ciphers. It is named after Julius Caesar, who is believed to have used it for communication with his generals during military campaigns. The basic principle behind the Caesar Cipher is the shifting of letters in the alphabet by a fixed number of positions.

The cipher operates by substituting each letter in the plaintext (the original message) with a letter that is a fixed number of positions down the alphabet. For example, with a shift of 3, 'A' would be encrypted as 'D,' 'B' as 'E,' and so on. When reaching the end of the alphabet, the counting wraps around to the beginning. So, with a shift of 3, 'X' would be encrypted as 'A,' 'Y' as 'B,' and 'Z' as 'C.'

To decrypt the message, the process is reversed. Each encrypted letter is shifted backward by the same number of positions. For example, if the shift was 3, 'D' would be decrypted as 'A,' 'E' as 'B,' and so on.

<br>

## What are the key differences between symmetric and asymmetric encryption? How is asymmetric used in secure communication today?
Symmetric encryption and asymmetric encryption are two fundamental types of encryption used in secure communication. Here are the key differences between them:

Key Usage: In symmetric encryption, the same secret key is used for both encryption and decryption. In contrast, asymmetric encryption uses a pair of mathematically related keys: a public key for encryption and a private key for decryption.

Key Distribution: With symmetric encryption, the shared secret key needs to be securely distributed to all parties involved in the communication. This can be challenging, especially when the number of participants is large. Asymmetric encryption addresses this issue by allowing the public keys to be freely distributed, while the private keys remain securely held by their respective owners.

Speed and Efficiency: Symmetric encryption algorithms are generally faster and more computationally efficient than asymmetric encryption algorithms. Asymmetric encryption involves more complex mathematical operations, making it slower and requiring more computational resources.

Security: Symmetric encryption provides confidentiality, but it lacks inherent authentication and non-repudiation features. Asymmetric encryption, on the other hand, offers not only confidentiality but also authentication and non-repudiation. The private key associated with the decryption can be used to verify the integrity of the encrypted message and authenticate the sender's identity.

Asymmetric encryption is commonly used in secure communication today in the following ways:

Key Exchange: Asymmetric encryption allows secure key exchange between parties who have never communicated before. For example, the Diffie-Hellman key exchange protocol uses asymmetric encryption to establish a shared secret key between two parties over an insecure channel.

Digital Signatures: Asymmetric encryption enables the creation and verification of digital signatures. A sender can use their private key to encrypt a hash of the message, providing integrity and non-repudiation. The recipient can verify the signature using the sender's public key.

Public Key Encryption: Asymmetric encryption is used for secure communication by encrypting data with the recipient's public key. Only the corresponding private key can decrypt the encrypted message. This allows for secure transmission of sensitive information over an insecure network.

Certificate Authorities (CAs): Asymmetric encryption plays a crucial role in the infrastructure of Certificate Authorities. CAs issue digital certificates that bind public keys to the identities of individuals or organizations. These certificates are used in various security protocols, such as SSL/TLS, to establish secure connections on the internet.

In summary, while symmetric encryption is efficient for bulk data encryption, asymmetric encryption is employed for key exchange, digital signatures, public key encryption, and establishing secure communication channels in modern systems.

<br>

## How do computers generate random numbers, and what are the differences between true random number generation (TRNG) and pseudo-random number generation (PRNG)? Discuss their use cases in cryptography.
Computers generate random numbers using two main approaches: true random number generation (TRNG) and pseudo-random number generation (PRNG).

True Random Number Generation (TRNG):
TRNG relies on physical processes to generate random numbers. These processes are typically based on unpredictable and inherently random natural phenomena, such as atmospheric noise, radioactive decay, or electronic noise. TRNGs capture these random events and convert them into random numbers. Since they rely on physical entropy sources, TRNGs can provide truly random and unpredictable numbers.
Use Cases in Cryptography:
TRNGs are well-suited for cryptographic applications that require high levels of security and unpredictability. They are commonly used for generating cryptographic keys, initialization vectors, and nonces. TRNGs are crucial for generating random values in cryptographic protocols, ensuring that the generated keys or values cannot be easily guessed or reproduced by an attacker.

<br>

## What’s the difference between encryption and decryption? Explain with an analogy.
Encryption and decryption are two processes used in cryptography to secure and protect sensitive information. Here's an analogy to illustrate the difference between encryption and decryption:

Let's imagine you have a locked box that contains a secret message. Encryption is like putting the message inside the box and locking it with a padlock. The message is transformed into an unintelligible form, known as ciphertext, using an encryption algorithm and a secret key. This process ensures that the contents of the message are hidden from anyone who doesn't possess the key. Just as the padlock prevents unauthorized access to the message, encryption prevents unauthorized access to the original information.

Now, for someone to read the message, they need to perform the reverse process, which is decryption. Decryption is like unlocking the padlock, opening the box, and revealing the original message. It involves using the same encryption algorithm and the correct key to transform the ciphertext back into the original plaintext. Decryption is the process of recovering the original information from the encrypted form.

To summarize, encryption is like locking the message in a box with a padlock, transforming it into ciphertext, while decryption is like unlocking the padlock, opening the box, and converting the ciphertext back into the original plaintext. Encryption ensures confidentiality and protects the information from unauthorized access, while decryption allows authorized parties to recover and understand the original message.

<br>

## Things I want to know more about :
Nothing for now .

