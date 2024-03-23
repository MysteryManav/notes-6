- It means producing uniform regions based on threshold criteria *T*. There are 3 types of thresholding:
	1. **Global**: Only on grayscale values
	2. **Local**: Neighbourhood property is considered
	3. **Dynamic**: Pixel coordinate is considered
- Thresholding is a function of:
	1. Spatial Coordinates: $(x, y)$
	2. Graylevel Coordinates: $f(x, y)$
	3. Local Property: $A(x, y)$
- $Th=T[x, y, f(x, y), A(x, y)]$
- Threshold can be found by histogram:
	1. **Unimodal Histogram**: ![[Unimodal.excalidraw]]
	2. **Bimodal Histogram**: ![[Bimodal.excalidraw]]
	3. **Multi-Modal Histogram**: ![[Multi-Modal.excalidraw]]
- **Single Level Thresholding**: It is attained by comparing pixel values
- If:
	1. $f(x, y)$ > T: Object
	2. $f(x, y)$ < T: Background

![[Single level thresholding.excalidraw]]

- **Multi Level Thresholding**: This is used to extract objects that have specific intensity range
- If:
	1. $T_1 \le f(x, y)$: One Object Class
	2. $T_2 \gt f(x, y)$: Other Object Class

![[Multi level thresholding.excalidraw]]

- **Global Thresholding**: Used for bimodal images  where histogram have two different peaks separated by a value. Valley point is the threshold 'T'. Pixels of a given image are compared with the threshold
- **Multiple Thresholding**: It divides the segments of a graylevel image into several distinct regions. Let, $f_i$ equal to value of input image pixel, $t_1, t_2, \dots, t_n$ be multiple threshold values, $g_1, g_2, \dots, g_n$ be output image pixel
$$
\text{Output Image} = \begin{cases}
g_1,\;if\;0 \le f_i \le t_1 \\
g_2,\;if\;t_1 \le f_i \le t_2 \\
\vdots \\
g_n,\;if\;t_{n-1} \le f_i \le 255
\end{cases}
$$
