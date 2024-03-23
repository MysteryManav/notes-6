- It is also known as derivative filter. The purpose of the sharpening spatial filter is just the opposite of the smoothing spatial filter. Its main focus in on the removal of blurring and highlight the edges. It is based on first and second order derivative
- **Edge Detectors**: They are also known as 'first-order derivatives'. An edge can be viewed as gradient calculator, which is extracted by computing the derivative of an image function. The magnitude of the derivative indicates the contrast of an edge. The direction of the derivative indicates orientation of an edge

### Second Order Derivative:
- In case of 2nd order derivative, the edge is present at a location, where 2nd derivative is zero. Two widely used 2nd order derivatives for edge detection are:
	1. Laplace of Gaussian (LoG)
	2. Canny

![[Sharpening Filters.excalidraw]]

### Laplacian Operator:
$$
\displaylines{
\nabla^2f(x, y) = \frac{\partial^2f(x, y)}{\partial x^2}\;+\;\frac{\partial^2f(x, y)}{\partial y^2} \\
\frac{\partial^2f}{\partial x^2} = f(x+1, y) - 2f(x, y) + f(x-1, y) \\
\frac{\partial^2f}{\partial y^2} = f(x, y+1) - 2f(x, y) + f(x, y-1)
}
$$

### Laplacian Masks:
$$
\displaylines{
\begin{bmatrix}
0 & -1 & 0 \\
-1 & 4 & -1 \\
0 & -1 & 0 \\
\end{bmatrix} \qquad
\begin{bmatrix}
-1 & -1 & -1 \\
-1 & 8 & -1 \\
-1 & -1 & -1 \\
\end{bmatrix} \\\\
\begin{bmatrix}
0 & 0 & -1 & 0 & 0 \\
0 & -1 & -2 & -1 & 0 \\
-1 & -2 & 16 & -2 & -1 \\
0 & -1 & -2 & -1 & 0 \\
0 & 0 & -1 & 0 & 0 \\
\end{bmatrix}
}
$$
