- It is also known as derivative filter. The purpose of the sharpening spatial filter is just the opposite of the smoothing spatial filter. Its main focus in on the removal of blurring and highlight the edges. It is based on first and second order derivative
- **Edge Detectors**: They are also known as 'first-order derivatives'. An edge can be viewed as gradient calculator, which is extracted by computing the derivative of an image function. The magnitude of the derivative indicates the contrast of an edge. The direction of the derivative indicates orientation of an edge

### First-Order Derivatives:
- **Gradient Operator**:
	- $$\displaylines{Vector\quad\nabla f = \begin{bmatrix}G_x\\G_y\end{bmatrix} = \begin{bmatrix}\partial f/\partial x\\\partial f/\partial y\end{bmatrix}\\ Magnitude\quad\nabla f = mag(\nabla f) = \sqrt{G_x^2 + G_y^2} = G \\ \text{Direction of Gradient} = tan^{-1}\begin{pmatrix}G_y \\ G_x\end{pmatrix}}$$
	- There are 3 types of Edge Detection Operators:
		1. **Robert Cross Edge Detector**: Known as Cross-Gradient Operator for diagonal Edges. Matrices are:$$G_x = \begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}\qquad G_y = \begin{bmatrix}0 & 1 \\ -1 & 0\end{bmatrix}$$
		2. **Prewitt Edge Detector**: For Vertical and Horizontal Edges$$G_x = \begin{bmatrix}-1 & 0 & 1 \\ -1 & 0 & 1 \\ -1 & 0 & 1\end{bmatrix}\qquad G_y = \begin{bmatrix}-1 & -1 & -1 \\ 0 & 0 & 0 \\ 1 & 1 & 1\end{bmatrix}$$
		3. **Sobel Edge Detector**: For Vertical and Horizontal Edges $$G_x = \begin{bmatrix}-1 & 0 & 1 \\ -2 & 0 & 2 \\ -1 & 0 & 1\end{bmatrix}\qquad G_y = \begin{bmatrix}1 & 2 & 1 \\ 0 & 0 & 0 \\ -1 & -2 & -1\end{bmatrix}$$
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

### Some Conditions:
- First Order Derivatives:
	1. Must be non-zero in flat segments
	2. Must be non-zero at onset of grey level step
	3. Must be non-zero along ramps
- Second Order Derivatives:
	1. Must be zero in flat areas
	2. Must be zero at the onset and end of ramp
	3. Must be zero along ramps
