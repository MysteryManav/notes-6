- Three basic Types:
	1. Linear (Negative and Identity Transformations)
	2. Logarithmic (log and inverse-log Transformations)
	3. Power Law ($n^{th}$ power and $n^{th}$ root transformation)

![[Intensity.excalidraw]]

0 -> L-1: Gray level
$'r'$: Input Intensity Level

### Linear Transformations:
1. **Image Negative**: Used for X-Rays, etc.$$S=L-1-r$$ S -> Gray level of Output Image; L -> Total Gray levels; r -> Gray level of Input Image
2. **Logarithmic**: Used for astronomy figures (Galaxy, etc.)$$S=C\times log(1 + r)$$ C -> Constant; $r \ge 0$
3. **Power Law**:$$S=C\times r^\gamma$$ C, r -> Positive Constant
	less $\gamma$ -> More Contrast
	Output Image:
		 $\gamma < 1$ -> More Contrast
		 $\gamma > 1$ -> Less Contrast

**NOTE**: Contrast is the difference between maximum and minimum graylevel
