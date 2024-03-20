- Done by encrypting plain-text with a key, $K_1$ and then encrypting the generated cipher-text with another key $K_2$ to generate the final cipher-text

### **Encryption**:
$$
C = E(K_2, E(K_1, P))
$$

### **Decryption**:
$$
P = D(K_1, D(K_2, C))
$$

### **Meet in the Middle Attack**:
- This attack involves encryption from one end, decryption from the other and matching the results in the middle
- Suppose crypt-analyst knows P and C. Now, the aim is to obtain the values of $K_1$ and $K_2$
- **Steps**:
	1. For all possible values ($2^{56}$) of key $K_1$, the crypt-analyst would encrypt the P by performing $E(K_1, P)$
	2. The outputs will then be stored in a table
	3. $C$ is then decrypted with all possible values of $K_2$
	4. All values generated from Step-3 are compared to the values of Cipher-text in $K_1$ to find the other key and plain-text
- **Formula**:
$$
X = E(K_1, P) = D(K_2, C)
$$
