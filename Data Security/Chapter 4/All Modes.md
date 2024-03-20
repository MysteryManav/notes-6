
### **Summary**:

| Operation Table | Description                                                                      |
| --------------- | -------------------------------------------------------------------------------- |
| [[ECB]]         | Each n-bit is encrypted independently with same key                              |
| [[CBC]]         | Same as E.C.B, but each block is XORed with previous cipher text                 |
| [[CFB]]         | Each s-bit block is XORed with s-bit key which is a part of previous cipher text |
| [[OFB]]         | Same as C.F.B, but the shift register is updated by the previous s-bit key       |
| [[CTR]]         | Same as O.F.B, but a counter is used instead of nonce                            |

### **Detail Comparison**:

| Parameter                    | [[ECB]]                      | [[CBC]]                                    | [[CFB]]                           | [[OFB]]                                 | [[CTR]]                                              |
| ---------------------------- | ---------------------------- | ------------------------------------------ | --------------------------------- | --------------------------------------- | ---------------------------------------------------- |
| *Parallelisation*            | Yes                          | No                                         | Partial (Only during Decryption)  | No                                      | Yes                                                  |
| *Block Dependency*           | Independent Blocks           | Each Block dependent on previous blocks    | Partial (Cipher of previous byte) | Partial (Encrypted Key and Nonce value) | Independent Blocks                                   |
| *Error Propagation*          | Limited (to affected block)  | Limited (to affected and subsequent block) | Limited (to affected byte)        | Limited (to affected byte)              | Limited (to affected block)                          |
| *Efficiency*                 | High                         | Modeerate                                  | Moderate                          | Moderate                                | High                                                 |
| *Initialisation Vector (IV)* | Not Required                 | Required and Must be Unique                | Required and Must be Unique       | Required and Must be Unique             | (Counter) Required, Must be Unique and Non-Repeating |
| *Security*                   | Weaker (Patterns may emerge) | Stronger (due to block dependencies)       | Moderate                          | Moderate                                | Strong (when using unique Nonces/Counters)           |
| *Suitability for Streams*    | Not Suitable                 | Not Suitable                               | Suitable                          | Suitable                                | Suitable                                             |
