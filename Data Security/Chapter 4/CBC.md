- It is a technique in which the same plain-text block, if repeated produces different cipher-text blocks
- In this scheme, the input to the encryption algorithm is the XOR of the current plain-text block and the preceding cipher-text block; the same key is used for each block
- To produce the first block of cipher-text, an initialisation vector (IV) is XORed with the first block of plain-text
- On decryption, the IV is XORed with the output of the decryption algorithm to recover the first block of plain-text

### **Process**:

![[Pasted image 20240317175319.png]]

### **Encryption**:
$$
C_1 = E(K, [P_1\;\oplus\;IV])
$$
$$
C_j = E(K, [P_j\;\oplus\;C_{j - 1}])\qquad|\qquad j = 2, ...., N
$$

### **Decryption**:
$$
P_1 = D(K, C_1) \oplus IV \\
$$
$$
P_j = D(K, C_j) \oplus C_{j-1}\qquad|\qquad j = 2, ...., N
$$

### **Advantages**:
- Works well for input greater than b bits
- It is a good authentication mechanism
- Better resistive towards crypt-analysis than E.C.B

### **Disadvantages**:
- Parallel Encryption not possible, as every encryption is dependent on previous cipher

### **Applications**:
- General purpose block oriented transmission
- Authentication
