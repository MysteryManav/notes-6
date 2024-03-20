- It is based on linear algebra
- Each letter is represented by numbers from 0 to 25 and calculations are done modulo 26
- Encryption and Decryption can be given by following formula:
- **Encryption**: $C = PK\;mod\;26$
- **Decryption**: $P = CK^{-1}\;mod\;26$
$$
(c_1, c_2, c_3) = (p_1, p_2, p_3) \begin{pmatrix} k11 & k12 & k13 \\ k21 & k22 & k23 \\ k31 & k32 & k33\end{pmatrix}
$$
- **Steps for Encryption**:
	1. Convert the key and plain-text into matrices
	2. Multiply the Matrices to obtain the Cipher-text using the formula above
- **Steps for Decryption**:
	1. Find Inverse of Key Matrix
	2. Multiply Multiplicative Inverse of Determinant by Adjoin Matrix
	3. Multiply inverse key matrix with cipher-text matrix to obtain plain-text matrix
