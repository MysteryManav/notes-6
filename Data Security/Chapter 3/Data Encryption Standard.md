- **Type**: Block Cipher
- **Block Size**: 64-bit
- **Key Size**: 64-bit, with only 56-bit effective
- **Number of rounds**: 16


	![[Pasted image 20240315131009.png]]

### **Algorithm**:
- First, the 64-bit plain-text passes through an **initial permutation** that rearranges the bits to produce the permuted input
- This is followed by a phase consisting of sixteen rounds of the same function, which involves both **permutation** and **substitution** functions
- Finally, the pre-output is passed through a permutation that is the **inverse of the initial permutation** function, to produce the 64-bit cipher-text
- The 56-bit key is passed through a **permutation function**
- For each of the sixteen rounds, a sub-key ($K_i$) is produced by the combination of a **left circular shift** and a **permutation**

	![[Pasted image 20240315210103.png]]
	#### **DES Single Round**

	![[Pasted image 20240315210239.png]]

- **Key Transformation**: Permutation of selection of sub-key from original key
- **Expansion Permutation (E-Table)**: Right half is expanded from 32-bits to 48-bits
- **S-box Substitution**: Accepts 48-bits from XOR operation and produce 32-bits using 8 substitution boxes (each S-boxes has a 6-bit input and 4-bit output)
- **P-box Permutation**
- **XOR and Swap**

### **Key-Side Expansion**:
- Initial key consists of 64-bits
- Before DES process starts, every 8th bit of key is discarded to produce a 56-bit key.
- Thus, discarding of every 8th bit key of the key produces a 56-bit key from original 64-bit key

### **Key Transformation**:
- The initial 64-bit is transformed into 56-bit key by discarding every 8th bit of initial key
- From 56-bit key, a different 48-bit sub-key is divided into two halves, each round using a process called key transformation
- For this, the 56-bit key is divided into two halves, each of 28 bits. These halves are circularly shifted left by one or two positions, depending on the round

### **Role of S-box**:
- The outer two bits of each group select one row of an S-box
- Inner four bits selects one column of an S-box

### **Avalanche Effect**:
- Desirable property of any encryption algorithm is that a change in one bit of the plain-text or of the key should produce a change in many bits of cipher-text
- DES performs *strong* avalanche effect

### **Key Generation in DES**:
![[Pasted image 20240315214018.png]]
- **DES Weak Keys**:
	1. Many block ciphers there are some keys that should be avoided, because of reduced cipher complexity
	2. These keys are such that same sub-key is generated in more than one round, and they include:
		1. **Weak Keys**: Same sub-key is generated for every round and DES has 4 weak keys
		2. **Semi-Weak Keys**: Only two sub-keys are generated on alternate rounds and DES has 12 of these
		3. **Demi-Semi Weak Keys**: Have four sub-keys generated
- None of these cause a problem since they are a tiny fraction of all available keys however they MUST be avoided by any key generation program

### **Advantages**:
- Widely Adopted
- Ease of Implementation
- Speed

### **Disadvantages**:
- Key Length
- Vulnerability to Brute Force
- Security Concerns

### **Possible Improvements for DES**:
- [[Multiple Encryption and Triple DES|Triple DES]]
- [[AES]]
- Key Management
- Use of Hardware Acceleration
- Hybrid Encryption
- Cryptographic Hash Functions
