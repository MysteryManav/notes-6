- An efficient way to find the GCD(a, b)
- Uses theorem:
		GCD(a, b) = GCD(b, a mod b)
- Euclid's Algorithm:
```
	int GCD(int A, int B)
		if (B == 0)
			return A;
		else
			return GCD(B, A % B)
```

- An extended version of this is used to [[Extended Euclidean Algorithm|Calculate the Inverse]] of modulo operation
