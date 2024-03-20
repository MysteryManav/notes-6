- Operates on blocks of data
- A block of plain-text is treated as a whole and used to produce a cipher-text block of equal length
- Typically, a block size of 64 and 128 bits is used
- Security of block ciphers depends on design of encryption function
- Software implementations of block ciphers runs faster than software implementation of stream ciphers
- **Examples**: Feistel Cipher, DES, Triple DES and AES
- One problem with cipher-text is that if same block of plain-text appears in two places, it encrypts to the same cipher-text. To avoid having these kinds of copies, feedback modes are used

### **Advantages**:
- High Diffusion
- Immunity to insertion of symbols

### **Disadvantages**:
- Slowness of encryption
- Error Propagation
