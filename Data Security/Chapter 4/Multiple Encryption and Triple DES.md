- Given the potential vulnerability of DES to a brute-force attack, there has been considerable interest in finding an alternative
- One approach is to design a completely new algorithm, of which [[Chapter 3/AES|AES]] is a prime example
- Another alternative, which would preserve the existing investment in software and equipment, is to use *multiple encryption with DES and multiple keys*

### **Triple DES**:
- There are two variations of Triple DES known as:
	1. 2-Key Triple DES
	2. 3-Key Triple DES

### **Two-Key Triple DES**
- **Encryption**:
- It involves processing the plain-text using [[Chapter 3/Data Encryption Standard|DES]] 3 times:
	1. First, the plain text is *encrypted* using the key $K_1$
	2. Second, the encrypted plain-text is then *decrypted* using the key $K_2$
	3. Lastly, the decrypted cipher-text is then *encrypted* again using the key $K_1$
$$
C = E(K_1, D(K_2, E(K_1, P)))
$$
- **Decryption**:
- It works the same way as during *Encryption*, with difference being:
	1. First, the cipher-text is *decrypted* using key $K_1$
	2. Second, the decrypted cipher-text is then *encrypted* again using key $K_2$
	3. Lastly, the encrypted cipher-text is then *decrypted* using key $K_1$
$$
P = D(K_1, E(K_2, D(K_1, C)))
$$

### **Three-Key Triple DES**:
- For 3-key Triple DES, a key K, which consists of different DES keys $K_1, K_2\;\text {and}\;K_3$  are generated. Hence, the key has length = $3 \times 56 = 168$ bits
- The Encryption and Decryption are done in similar way to DES, i.e, the plain-text is encrypted first using $K_1$, then $K_2$ and at last $K_3$ and for decryption the reverse is followed
