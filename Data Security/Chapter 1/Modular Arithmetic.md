- **Define Modulo (%) operator**: $\text {a mod n}$ is defined to be remainder when $a$ is divided by $n$
- Use the term *congruence* for $a \equiv \text {b mod n}$
	- when divided by $n$, $a$ and $b$ have same remainder
- $r$ is called residue of $\text {a mod n}$: $\text { a = nq + r}$ , usually, $0 <= r < n; q = [a/n]$
- $Z_n$ is set of residues or residue classes, i.e., $[r]=\{a : \text {a is an integer}, a \equiv r\;mod\;n\}$
- Residue Class is represented by the smallest non-negative number in the class

### **Properties of Congruence**:
- $a \equiv \text {b mod n}$ iff $n | (a - b)$
- $a \equiv \text {b mod n}$ implies $b \equiv \text {a mod n}$
- $a \equiv \text {b mod n}$ and $b \equiv \text {c mod n}$ implies $a \equiv \text {c mod n}$

### **Modular Arithmetic Properties**:
- **Commutative Laws**:
	1. $\text {(w + x) mod n} = \text {(x + w) mod n}$
	2. $(w \times x)\,mod\,n = (x \times w)\,mod\,n$
- **Associative Laws**:
	1. $[(w + x) + y]\;mod\;n = [w + (x + y)]\;mod\;n$
	2. $[(w \times x) \times y]\;mod\;n = [w \times (x \times y)]\;mod\;n$
- **Distributive Laws**: $[w \times (x + y)]\;mod\;n = [(w \times x) + (w \times y))]\;mod\;n$
- **Identities**:
	1. $(0 + w)\;mod\;n = w\;mod\;n$
	2. $(1 \times w)\;mod\;n = w\;mod\;n$
- **Additive Inverse (- w)**: For each  $w \in Z_n$ , there exists a $z$ such that $w + Z \equiv 0\;mod\;n$
- **Addition**: $(a + b)\;(mod\;m) \equiv (a\;(mod\;m) + b\;(mod\;m))\;(mod\;m)$
- **Subtraction**: $(a - b)\;(mod\;m) \equiv (a\;(mod\;m) - b\;(mod\;m))\;(mod\;m)$
- **Multiplication**: $(a \cdot b)\;(mod\;m) \equiv (a\;(mod\;m) \cdot b\;(mod\;m))\;(mod\;m)$
- **Exponentiation**: $(a^n)\;(mod\;m) \equiv (a\;(mod\;m)^n\;(mod\;m)$

### **Divisors**:
- Say a non-zero number b divides a, if for some $m$, we have $a = m \cdot b$, i.e., b divides into a with no remainder, then we can denote it as $b\;\vert\;a$ and say that b is a divisor of a
- **Properties of Divisors**:
	1. If $a\;\vert\;1$ then a = 1 or -1
	2. If $a\;\vert\;b$ and $b\;\vert\;a$ then a = b or a = -b
	3. Any b <> 0 then $b\;\vert\;0$
	4. If $b\;\vert\;g$ and $b\;\vert\;h$ then $b\;\vert\;(mg + nh)$

