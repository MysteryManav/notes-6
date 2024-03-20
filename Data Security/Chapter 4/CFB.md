- It is possible to convert a block cipher into a stream cipher, using Cipher Feedback (C.F.B) mode, Output Feedback (O.F.B) mode and Counter (C.T.R) mode
- A stream cipher eliminates the need to pad a message to be an integral number of blocks
- It can operate in real time

### **Encryption**:
- Input to encryption function is a 64-bit register that is initially set to some initialisation vector (IV)
- The M.S.B. (left-most) '*s*' bits of the output of encryption function are XORed with the firs segment of the plain-text $P_1$ to produce the first unit of cipher-text $C_1$, which is then transmitted
- In addition, the contents of the shift register are shifted left by '*s*' bits and $C_1$ (the previous cipher) is placed in the rightmost '*s*' bits of the shift register
- This process continues until all the plain-text units have been encrypted
$$
\displaylines {
I_1 = IV \\
I_j = LSB_{b - s}(I_{j - 1}) || C_{j - 1}\qquad j = 2, ...., N \\
O_j = E(K, I_j)\qquad j = 1, ...., N \\
C_j = P_i \oplus MSB_s(O_j)\qquad j = 1, ...., N
}
$$

![[Pasted image 20240317182738.png]]

### **Decryption**:
- The same scheme is used except that the received cipher-text unit is XORed with the output of the encryption function to produce the plain-text unit
$$
\displaylines {
I_1 = IV \\
I_j = LSB_{b - s}(I_{j - 1}) || C_{j - 1}\qquad j = 2, ...., N \\
O_j = E(K, I_j)\qquad j = 1, ...., N \\
P_j = C_i \oplus MSB_s(O_j)\qquad j = 1, ...., N
}
$$

![[Pasted image 20240317182910.png]]

### **Advantages**:
- Since there is some data loss due to use of shift register, it is difficult during crypt-analysis

### **Disadvantages**:
- Both block losses and concurrent encryption of several blocks are not supported by encryption.
- Decryption, however, is parallelizable and loss-tolerant
