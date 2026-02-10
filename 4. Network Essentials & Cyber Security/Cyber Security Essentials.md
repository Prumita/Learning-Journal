# Topic 2: Cyber Security Essentials

## CIA Triad

C - Confidentiality
I - Integrity
A - Availability

## NIST Cybersecurity Framework
Government agency that coordinates and looks at cyber security framework. They are also a regulator who will help you to identify what the areas are that are important.

## Multi-Factor authentication
The principles of MFA is that you need to have 2 of the following:

- What you know (password, PIN)
- What you have (device)
- Who you are (biometric, fingerprint)

So password + PIN is not MFA, because they are both just 'what you know'. But if an app has given you a pin code, then that pin code is 'what you have' and a password would be 'what you know' and that would be fine. But if it's just a password and pin you have set yourself, that's not MFA.

## Encryption
So you have a symmetric encryption, wehre the same key is used to encrypt and decrypt the data. Must use the same one for both else it won't decrypt.

There is also asymmetric, where there is a source and destination key, or public and private key.
Analogy here is a PO Box, you can give the address to as many people as you want, it's public. 
Sending a letter,  you put the public key there, the PO box. Can be sent to the post office, and the post office guy will put it in your box. You're supposed to then have a key to open that particular box. 
Private key is another algorithm. How does the private key get generated? It's completely different to the public key.
Private key, not shared. Private key can also be used to encrypt, but only it can be used to decrypt. So you could give someone your public key to send you something encrypted, but only you can decrypt with your private key. So anyone intercepting that encryption cannot use anything, unless they somehow also use the private key.
Much better than symmetric, seen as for example there are websites that let you encrypt and decrypt with symmetric keys! So you could presumably just decrypt with each of them until one works.

## Hashing

Different to encryption, there is no going back. So if you use hash it is a representation of that data. You cannot decode it back into its original form. I dunno how?
With hashing, the size of the data does not matter. It matters a lot with encryption.
For example cryptography, every character represented by another character, of course more data is going to mean more encryption.
