### **Design Principles of Block Cipher**:
- Criteria for S-box are as follows:
	1. No output bit of any S-box should be too close a linear function of input bits
	2. Each row of S-box should include all 16 possible output bit combinations
	3. If two inputs to an S-box differ in exactly one bit, the outputs must differ in at least two bits
	4. If two inputs to an S-box differ in two middle bits exactly, the outputs must differ in at least two bits
	5. If two inputs to an S-box differ in their first two bits and are identical in their last two bits, the two outputs must not be same
	6. For any non-zero 6-bit difference b/w inputs, no more than 8 of the 32 pairs of inputs exhibiting the difference may result in same output difference
- Criteria for Permutation, P, are as follows:
	1. Four output bits from each S-box at round 'i' are distributed so that two of them affect middle bits of round (i + 1) and other two affect end bits
	2. Four output bits from each S-box affect six different S-boxes on the next round, and no two affect the same S-box
	3. For two S-boxes, j, k, if an output bit from S; affects a middle bits of Stock on the next round, then an output bit from $S_k$ cannot affect a middle bit of $S_j$
