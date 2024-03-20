- A **Stream Cipher** is one that encrypts a digital data stream one bit or one byte at a time
- **Examples of Classical Stream Ciphers**: Auto-keyed Vigenere Cipher, A5/1, RC4 and Vernam Cipher
- It is similar to one-time pad
- It encrypts smaller block of data, typically bits or bytes
- A key stream generator outputs a stream buts $K_1, K_2, K_3, ...., K_i$
- This key stream is XORed with a stream of plain-text bits $P_1, P_2, P_3, ...., P_i$ to produce the stream of cipher-text bits: $C_i = P_i \oplus K_i$
- At the description end, the cipher-text bits are XORed with an identical key stream to recover the plain-text bits: $P_i = C_i \oplus K_i$
- System security depends entirely on key-stream generator

### **Advantages**:
- Speed of Transmission
- Low Error Propagation

### **Disadvantages**:
- Low Diffusion
- Susceptibility to malicious insertion and modifications
