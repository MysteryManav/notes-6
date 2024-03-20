- **Cryptanalysis**: Crypt-analytic attacks rely on nature of algorithm and some knowledge of general characteristics of the plain-text or even some sample plain text-cipher text pairs
- This type of attack exploits the characteristics of algorithm to attempt to derive a specific plain text or to derive the key being used

- **Brute Force Attack**: The attacker tries every possible key on a piece of cipher text until an intelligible translation into plain text is obtained

- **Attacks on Encrypted Messages**:

| Type of Attack         | Known to Crypt-analyst                                                                                                                                                                                                                        |
|:---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Cipher-text Only**   | Encryption Algorithm, Cipher-text                                                                                                                                                                                                             |
| **Known Plain-text**   | Encryption Algorithm, Cipher-text, One or more plain text-cipher text pairs formed with secret key                                                                                                                                            |
| **Chosen Plain-text**  | Encryption Algorithm, Cipher-text, Plain-text message chosen by crypt-analyst                                                                                                                                                                 |
| **Chosen Cipher-text** | Encryption Algorithm, Cipher-text, Cipher-text chosen by crypt-analyst with its corresponding decrypted plain text generated with secret key                                                                                                  |
| **Chosen Text**        | Encryption Algorithm, Cipher-text, Plain-text chosen by crypt-analyst with its corresponding cipher-text generated with secret key, Cipher-text chosen by crypt-analyst with its corresponding decrypted plain-text generated with secret key |
