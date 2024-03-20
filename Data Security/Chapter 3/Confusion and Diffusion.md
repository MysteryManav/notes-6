### **Diffusion (CT, PT)**:
- It hides the relationship between the cipher-text and the plain-text
- Achieved by having each plain-text digit affect the value of many cipher-text digits

### **Confusion (CT, KEY)**:
- It hides the relationship between cipher-text and key
- Achieve by use of a complex substitution algorithm

### **Difference b/w Diffusion and Confusion**:

| Diffusion                                                                                                                    | Confusion                                                                                                               |
| ---------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Hides relation b/w cipher-text and plain-text                                                                                | Hides relation b/w cipher-text and key                                                                                  |
| If single symbol in plain-text changed, several or all symbols in cipher-text will also be changed                           | If single bit in key changed, most or all bits in cipher-text will also be changed                                      |
| Statistical structure of plain-text is dissipated into long-range statistics of cipher-text. <br><br>Achieved by permutation | Relationship b/w statistics of cipher-text and value of encryption key is made complex.<br><br>Achieved by substitution |