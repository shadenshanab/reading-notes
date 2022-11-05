# class 16

## Encryption

--------------

## Encryption, decryption, and cracking

### Thanks to this exploration of the Caesar Cipher, we now understand the three key aspects of data encryption:

- Encryption: scrambling the data according to a secret key (in this case, the alphabet shift).
- Decryption: recovering the original data from scrambled data by using the secret key.
- Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.

## Encrypting a message

### One of the earliest encryption techniques is the Caesar Cipher, invented by Julius Caesar more than two thousand years ago to communicate messages to his allies.

### The Caesar Cipher is a great introduction to encryption, decryption, and code cracking, thanks to its simplicity.

### The Caesar Cipher is a simple substitution cipher which replaces each original letter with a different letter in the alphabet by shifting the alphabet by a certain amount.

## Decrypting a message

### According to historical records, Caesar always used a shift of 3. As long as his message recipient knew the shift amount, it was trivial for them to decode the message.

## Cracking the cipher

### Frequency analysis

#### Human languages tend to use some letters more than others. For example, "E" is the most popular letter in the English language. We can analyze the frequency of the characters in the message and identify the most likely "E" and narrow down the possible shift amounts based on that.

### Known plaintext

#### Another term for the original unencrypted message is plaintext. If the enemy already knew some part of the plaintext, it will be easier for them to crack the rest of the encrypted version.

#### For example, messages tend to start with similar beginnings. In WWII, encrypted German messages always started with a weather forecast, which ultimately made them easier for British mathematician Alan Turing to crack.

### Brute force

#### There are only 25 possible shifts (not 26 — why not?). The enemy could take some time to try out each of them and find one that yielded a sensible message. They wouldn't even need to try the shifts on the entire message, just the first word or two.