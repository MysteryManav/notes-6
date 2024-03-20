
| Stream Cipher                                                               | Block Cipher                                                              |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| Operate on smaller units of plain-text                                      | Operate on large block of data                                            |
| Faster than block cipher                                                    | Slower than stream cipher                                                 |
| Processes input element continuously producing output one element at a time | Processes input block wise producing an output block for each input block |
| Less code                                                                   | More code                                                                 |
| One time of key use                                                         | Reuse of key possible                                                     |
| **Example**: [[Chapter 2/One-Time Pad\|One Time Padding]]                   | **Example**: [[Chapter 3/Data Encryption Standard\|DES]], [[AES]]         |
| **Applications**: SSL, etc.                                                 | **Applications**: Database File Encryption                                |
| More suitable for hardware implementation                                   | Easier to implement in software                                           |
