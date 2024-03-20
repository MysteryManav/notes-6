- It is done in the neighbourhood of the pixels. It is linear or non-linear in nature. Two types of spatial filters:
	1. Correlation
	2. Convolution
- Both are linear
- Correlation/Convolution is a process of moving a filter mask over the image and computing sum of products for each pixel
- They are used to check similarity between 2 images (whole or part)
- If the image size is $(M \times N)$, the mask size is $(m \times n)$, where $m = 2a + 1$ and $n = 2b + 1$, where 'a' and 'b' are integer
- Smallest value for $(m \times n)$ is $(3 \times 3)$

### Part of an image:

![[Part of an image.excalidraw]]

### Mask:

![[Mask.excalidraw]]

### Equation Representing a Spatial Filter:
$$
\displaylines{
g(x, y) = w(-1, -1)\cdot f(x-1, y-1) + w(-1, 0)\cdot f(x-1, y) + \dots + w(0, 0)\cdots f(x, y) + \dots + w(1, 1)\cdots f(x+1, y+1) \\
= \sum_{s=-a}^a\sum_{t=-b}^bw(s, t)\cdot f(x + s, y + t)
}
$$
- 'x' and 'y' are varied such that 'w' visits every location in 'f'

### Correlation:
- To calculate value and match for corner or boundary pixels, there are 2 methods:
	1. Zero Padding
	2. Overlapped Boundary (Wrap Around)

### Convolution:
- It is like correlation except the mask is rotated by $180\degree$ vertically and horizontally
