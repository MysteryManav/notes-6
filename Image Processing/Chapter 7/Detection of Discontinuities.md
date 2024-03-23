- Image segmentation algorithms are based on 2 principles:
	1. The disconitnuity principle
	2. The similarity principle
- Discontinuity principles are of 4 types:
	1. Point Detection
	2. Line Detection
	3. Edge Detection
	4. Corner Detection
- Edge Detection is an approach used frequently for segmenting images based on abrupt change in intensity. They are of 3 types:
	1. **First-Order Derivative**: Used for thicker lines and masks are: *Robert-Cross*, *Prewitt* and *Sobel*
	2. **Second-Order Derivative**: Used for thinner lines and masks are: *Laplacian (LoG)* and *Canny*
	3. **Kirsch-Compass**: There are 7 masks used for finding maximum edge strength in determined directions. They are:
		1. *North Mask: N* $$\begin{matrix}-3 & -3 & 5 \\-3 & 0 & 5 \\-3 & -3 & 5 \end{matrix}$$
		2. *North West Mask: NW* $$\begin{matrix}-3 & 5 & 5 \\-3 & 0 & 5 \\-3 & -3 & -3 \end{matrix}$$
		3. *West Mask: W* $$\begin{matrix}5 & 5 & 5 \\-3 & 0 & -3 \\-3 & -3 & -3 \end{matrix}$$
		4. *South West Mask: SW* $$\begin{matrix}5 & 5 & -3 \\5 & 0 & -3 \\-3 & -3 & -3 \end{matrix}$$
		5. *South Mask: S* $$\begin{matrix}5 & -3 & -3 \\5 & 0 & -3 \\5 & -3 & -3 \end{matrix}$$
		6. *South East Mask: SE* $$\begin{matrix}-3 & -3 & -3 \\5 & 0 & -3 \\5 & 5 & -3 \end{matrix}$$
		7. *East Mask: E* $$\begin{matrix}-3 & -3 & -3 \\-3 & 0 & -3 \\5 & 5 & 5 \end{matrix}$$
		8. *North East Mask: NE* $$\begin{matrix}-3 & -3 & -3 \\-3 & 0 & 5 \\-3 & 5 & 5 \end{matrix}$$