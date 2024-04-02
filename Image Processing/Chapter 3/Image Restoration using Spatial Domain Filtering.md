### Restoration of Image in presence of Noise only:
- Degradation only due to noise in spatial domain can be represented as:$$g(x, y)=f(x, y) + n(x, y)$$
- In Fourier domain, the equation becomes:$$G(u, v) = F(u, v) + N(u, v)$$
- There are 2 types of filters for restoring an image in presence of noise only:
	1. Mean Filter
	2. Order Statistics Filter
- Mean Filter:
	1. Arithmetic Mean Filter (A.M.F):$$\hat f(x, y) = \frac{1}{mn}\sum_{(r, c) \in S_{xy}}g(r, c)$$
		- $g(x, y)$ => Corrupted Image
		- $r, c$ => Row and Column Co-ordinates of pixel in neighbourhood $S_{xy}$
		- Size of Kernel => $m \times n$
		- $S_{xy}$ => Set of co-ordinates on rectangular sub-images of size $m \times n$ centred at $(x, y)$
		- A.M.F is used to smoothen the local variation and to reduce noise due to blurring
	2. Geometric Mean Filter (G.M.F):$$\hat f(x, y) = \left[ \prod_{(r, c) \in S_{xy}}g(r, c) \right]^{\frac{1}{mn}}$$
		- In G.M.F, less image details are lost compared to A.M.F
	3. Harmonic Mean Filter (H.M.F):$$\hat f(x, y) = \frac{mn}{\sum_{(r, c) \in S_{xy} \frac{1}{g(r, c)}}}$$
		- H.M.F works well for salt noise and Gaussian noise and fails for pepper noise
	4. Contra-Harmonic Mean Filter:$$\hat f(x, y)=\frac{\sum_{(r, c) \in S_{xy}}g(r, c)^{Q+1}}{\sum_{(r, c) \in S_{xy}}g(r, c)^Q}$$
		- Q => Order of Filters
		- Q = Positive =>Eliminates Pepper Noise
		- Q = Negative => Eliminates Salt Noise
- Order Statistics Filter: The respond of an order statistics filter is based on ordering or ranking of pixels
	1. Median Filter:$$\hat f(x, y) = \underset{(r, c) \in S_{xy}}{median} \{g(r, c)\}$$
		- The median filter is an excellent noise reduction with less blurring
		- It is effective in presence of bi-polar and uni-polar impulse noise
	2. Min/Max Filter:$$\hat f(x, y) = \underset{(r, c) \in S_{xy}}{min/max} \{g(r, c)\}$$
		- The *max* filter is used for finding the brightest point in an image
		- The *min* filter is used for finding the darkest point of an image
	3. Mid-Point Filter:$$\hat f(x, y) = \frac{1}{2}\left[\underset{(r, c) \in S_{xy}}{max}\{g(r, c)\} + \underset{(r, c) \in S_{xy}}{min}\{g(r, c)\} \right]$$
		- The mid-point filter computes the mid-point between max and min values in the area encompassed by the filter
		- It works best for randomly distributed noise like Gaussian noise and uniform noise
	4. Alpha-Trimmed Mean Filter:$$\hat f(x, y)=\frac{1}{mn - d}\sum_{(r, c) \in S_{xy}}g_R(r, c)$$
		- $d \in [0, mn-1]$
		- For implementing Alpha-trimmed Mean Filter:
			1. Remove $\frac{d}{2}$ lowest and $\frac{d}{2}$ highest intensity values for $g(r, c)$
			2. $g_R(r, c)$ => remaining $(mn - d)$ pixel in $S_{xy}$
		- The Alpha-trimmed Mean Filter is used for removing the combination of salt and pepper and gaussian noise
### Adaptive Filters in Image Processing:
- **Adaptive Local Noise Reduction**: It involves the mean value of gray level denoted by $\mu$ and the contrast of the gray level denoted by $\sigma$. The filter is based on 4 quantities:
	1. $g(x, y)$ => Value of noisy image $(x, y)$
	2. $\sigma_n^2$ => Variance of the noise corrupting $f(x, y)$ to form $g(x, y)$
	3. $m_L$ => Local mean of the pixels in the neighbourhood $S_{xy}$
	4. $\sigma_L^2$ => Local variance of the pixel in the neighbourhood $S_{xy}$
$$
f(x, y) = g(x, y) - \frac{\sigma_n^2}{\sigma_L^2}\left[ g(x, y) - m_L\right]
$$
- **Adaptive Median Filter**: The median filter works only when the noise is not large, i.e., $P_a$ and $P_b$ is less than 0.2 
	- Adaptive Median Filter handles the impulse noise of larger values
	- It preserves the detail of image, thereby smoothing the non-impulse noise
	- Let,
		1. $z_{min}$ => Min of gray level in $S_{xy}$
		2. $z_{max}$ => Max of gray level in $S_{xy}$
		3. $z_{median}$ => Median of gray level in $S_{xy}$
		4. $S_{max}$ => Max allotted size of $S_{xy}$
		5. $A_1 = z_{median} - z_{min}$
		6. $A_2 = z_{median} - z_{max}$
	- Algorithm:
$$
\displaylines{
\text{Level A}
\begin{cases}
\begin{align*}
& \text{if } A_2 < 0 \le A_1 \\
& \quad\text{Go to level B} \\
& \text{else} \\
& \quad\text{Increase Window Size} \\
& \quad\text{if window} \le S_{max} \\
& \quad\quad\text{repeat level A} \\
& \quad\text{else} \\
& \quad\quad\text{Output} = z_{xy}
\end{align*}
\end{cases} \\
\qquad\qquad\quad\text{Level B}
\begin{cases}
\begin{aligned}
& B_1 = z_{xy} - z_{\text{min}}; \quad B_2 = z_{xy} - z_{\text{max}} \\
& \text{if } B_2 \le 0 \le B_1 \\
& \quad \text{O/p} = z_{xy} \\
& \text{else} \\
& \quad \text{O/p} = z_{\text{median}}
\end{aligned}
\end{cases}
}
$$
