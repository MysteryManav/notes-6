- It is easiest block cipher mode of functioning. It is easier because of direct encryption of each block of input plain-text and output is in form of blocks of encrypted cipher-text.
- In E.C.B. Mode, plain-text is handled one block at a time and each block of plain-text is encrypted using the same key
- The term *codebook* is used because, for a given key, there is a unique cipher-text for every b-bit block of plain-text

### **Process**:

![[Pasted image 20240317150309.png]]

### **Encryption**:
$$
C_j = E(K, P_j);\qquad\text{j = 1, ...., N}
$$

### **Decryption**:
$$
P_i = D(K, C_j);\qquad\text{j = 1, ...., N}
$$

### **Advantages**:
- Simple
- Parallel Encryption of blocks of bits is possible, thus it is a faster way of encryption

### **Disadvantages**:
- Prone to crypt-analysis, since there is direct relationship between plain-text and cipher-text
- Repetitive information contained in plain-text may show in cipher-text, if aligned with blocks
- If message has repetitive elements, with a period of repetitions a multiple of b-bits, then these elements can be identified by the analyst

### **Applications**:
- Secure transmission of short pieces of information, like a temporary encryption key
- 
