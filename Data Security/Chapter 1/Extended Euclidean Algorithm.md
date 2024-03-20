- Extends Euclid's Algorithm
- Used to calculate inverse of a modulo operation
- Extended Euclid's Algorithm:
```
	EXTENDED_EUCLID(m, b)
		(A1, A2, A3) = (1, 0, m)
		(B1, B2, B3) = (0, 1, b)
		if B3 == 0
			return A3 = GCD(m, b) //no inverse
		if B3 == 1
			return B3 = GCD(m, b); B2 = b^-1 mod m
		Q = A3 div B3
		(T1, T2, T3) = (A1 - Q*B1, A2 - Q*B2. A3 - Q*B3)
		(A1, A2, A3) = (B1, B2, B3)
		(B1, B2, B3) = (T1, T2, T3)
```
- The original version of this algorithm is used to [[Euclidean Algorithm|Calculate the GCD of two numbers]]
