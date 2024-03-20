- More popular and widely adopted symmetric encryption algorithm likely to be encountered nowadays is the A.E.S. It is found at least six times faster than triple D.E.S
- Features:
	1. Symmetric Key, Symmetric Block Cipher
	2. 128-bit data, 128/192/256-bit keys
	3. Stronger and faster than Triple-DES
	4. Provide full specifications and design details
- Characteristics:
	1. Resistance against all known attacks
	2. Speed and Code compactness on a wide range of platforms
	3. Design Simplicity

### Structure:

![[Pasted image 20240319214815.png]]

- Initialisation:
	1. Expand 16-byte key to get the actual key block to be used.
	2. Initialise 16-byte plain-text block called as state.
	3. XOR the state with the key block.
- For each round:
	1. Apply S-box
	2. Rotate rows of state
	3. Mix Columns (Not in the last round)
	4. Add Round Key: XOR the state with key block

### A.E.S Structure:
- The first N-1 rounds consist of four distinct transformation functions:
	1. *SubBytes*: The 16 input bytes are substituted using an S-box
	2. *ShiftRows*: Each of the four rows of the matrix is shifted to the left. The first row is not altered; For second row, a 1-byte circular left shift is performed; For third row, a 2-byte circular left shift is performed; For fourth row, a 3-byte circular left shift is performed
	3. *MixColumns*: Each column of four bytes is now transformed using a special mathematical function
	4. *AddRoundKey*: The 16 bytes of the matrix are now considered as 128 bits and are XORed to the 128 bits of the round key
