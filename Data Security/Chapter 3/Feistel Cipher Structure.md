- **Input**: Block of length $2w$ bits
- **Key**: $n$ bits
- **Sub-Keys**: $K_1, K_2, ...., K_n$
- All rounds have same structure
- This structure is called **Substitution-Permutation Network (S.P.N.)**

### **Steps**:
1. Plain-text (of size $2w$ bits) is divided into 2 equal blocks of $w$ bits each, namely, $L_i$ and $R_i$
2. A *substitution* is performed by taking exclusive-OR (XOR) on Left half of data, $L_i$ and output of round function $F$ which has inputs Right half, $R_i$ and key $K_i$
3. A *permutation* is performed that consists of interchange of two halves of data

### **Feistel Network Factors**:
- **Block Size**: Common block size of 64-bit. However, new algorithms use 128-bit, 256-bit block size
- **Key Size**: Key sizes of 64-bits or less are widely considered insufficient and hence, at least 128-bit, or 192-bit or 256-bit keys are used
- **Number of rounds**: A typical size is 16 rounds
- **Round Function, F**: Greater complexity means greater resistance to crypt-analysis and attacks
- **Sub-key generation algorithm**: Greater complexity in algorithm should lead to greater difficulty of crypt-analysis
