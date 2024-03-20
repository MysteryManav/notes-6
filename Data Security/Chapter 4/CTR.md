- It has increased recently with applications to ATM (Asynchronous Transfer Mode), Network Security and IP security
- A counter equal to plain-text block size is used
- Counter value must be different for each plain-text block that is encrypted
- Typically, counter is initialised to some value and then incremented by 1 for each subsequent block

### **Encryption**:

![[Pasted image 20240317191920.png]]

### **Decryption**:

![[Pasted image 20240317191943.png]]

### **Advantages**:
- Needs only encryption algorithm
- Random access to encrypted data blocks
- Blocks can be processed in parallel
- Simple
- Fast Encryption/Decryption

### **Disadvantages**:
- A synchronous counter at both transmitter and the receiver is a severe drawback
- The recovery of plain-text is erroneous when synchronisation is lost

### **Counter must be**:
1. Unknown and Unpredictable
2. Pseudo-randomness in the key stream is a goal
