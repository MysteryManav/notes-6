- Three types of Discontinuities:
	1. Point
	2. Line
	3. Edge
- For Point Detection: $$R = \sum_{i=1}^a w_iz_i$$ If $\lvert R\rvert \ge T$; a point is detected; T is non-negative
$$\displaylines{
\text{Mask} = \begin{bmatrix}
w_1 & w_2 & w_3 \\
w_4 & w_5 & w_6 \\
w_7 & w_8 & w_9 
\end{bmatrix} \\
\text{Image} = \begin{bmatrix}
z_1 & z_2 & z_3 \\
z_4 & z_5 & z_6 \\
z_7 & z_8 & z_9 
\end{bmatrix} \\
\text{Sample mask for point detection} = \begin{bmatrix}
-1 & -1 & -1 \\
-1 & 8 & -1 \\
-1 & -1 & -1
\end{bmatrix}
}$$
- Four types of Masks for line detection:
$$
\displaylines{
\text{Horizontal} = \begin{bmatrix}
-1 & -1 & -1 \\
2 & 2 & 2 \\
-1 & -1 & -1
\end{bmatrix} \\
+45\degree = \begin{bmatrix}
-1 & -1 & 2 \\
-1 & 2 & -1 \\
2 & -1 & -1
\end{bmatrix} \\
\text{Vertical} = \begin{bmatrix}
-1 & 2 & -1 \\
-1 & 2 & -1 \\
-1 & 2 & -1
\end{bmatrix} \\
-45\degree = \begin{bmatrix}
2 & -1 & -1 \\
-1 & 2 & -1 \\
-1 & -1 & 2
\end{bmatrix}
}
$$
- **Edge Detectors**: They are known as first-order derivatives. An edge can be viewed as gradient calculator, which is extracted by computing the derivative of an image function. The magnitude of the derivative indicates the contrast of an edge. The direction of the derivative indicates orientation of an edge
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
