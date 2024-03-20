- The A.E.S key expansion algorithm takes as input a four-word (16-byte) key and produces a linear array of 44 words (176 bytes)
- Each added word $w[i]$ depends on the immediately preceding word, $w[i - 1]$
- In three out of four cases, a simple XOR is used

![[Pasted image 20240319220507.png]]
