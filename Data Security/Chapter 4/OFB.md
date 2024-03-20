- The output feedback (O.F.B) mode is similar in structure to that of C.F.B
- For O.F.B, the output of encryption function is fed back to become the input for encrypting the next block of plain-text, while, in C.F.B, the output of the XOR unit is fed back to become input for encrypting the next block
- Other difference is that O.F.B mode operates on full blocks of plain-text and cipher-text, whereas, C.F.B operates on an '*s-bit*' subset
- Each bit in cipher-text is independent of previous bit or bits
- Pre-Compute pr 
- **Nonce**: A time-varying value that has at most a negligible chance of repeating, for example, a random value that is generated anew for each use, a timestamp, a sequence number, or some combination of these

### **Encryption**:

![[Pasted image 20240317184451.png]]

$$
\displaylines {
I_1 = Nonce \\
I_j = O_{j - 1}\qquad j = 2, ...., N \\
O_j = E(K, Nonce)\qquad j = 1, ...., N \\
C_j = P_j \oplus O_j\qquad j = i, ...., N - 1 \\
C^*_N = P^*_N \oplus MSB_u(O_N)
}
$$

### **Decryption**:

![[Pasted image 20240317184516.png]]

$$
\displaylines {
I_j = Nonce \\
I_j = O_{j - 1}\qquad j = 2, ...., N \\
O_j = E(K, I_j)\qquad j = 1, ...., N \\
P_j = C_j \oplus O_j\qquad j = 1, ...., N - 1 \\
P^*_N = C^*_N \oplus MSB_u(O_N)
}
$$

### **Advantages**:
- In C.F.B, single bit error in a block is propagated to all subsequent blocks, while, in O.F.B as it is free from bit errors in the plain-text blocks

### **Disadvantages**:
- Because to its operational modes, it is more susceptible to a message stream modification attack than C.F.B
