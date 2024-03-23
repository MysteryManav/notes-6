### Gaussian Noise:
$$
PDF = P(z) = \frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(z - u)^2}{2\sigma^2}}
$$
where, 
- $z$ => graylevel
- $\mu$ => Mean of $z$
- $\sigma$ => Standard Deviation
- ![[Pasted image 20240322230639.png]]
- $\bar z$ => is the mean of $z$ or $\mu$

### Rayleigh Noise:
$$
P(z) = \begin{cases}
\frac{2}{b}(z - a)^{-\frac{(z-a)^2}{b}} & \text{for z $\ge$ a} \\ \\
0 & \text{for z $\lt$ a}
\end{cases}
$$
- a, b => non-negative integers
- $\mu = a + \sqrt{\frac{\pi b}{4}}$
- $\sigma^2 = \frac{b(4 - \pi)}{4}$
- ![[Pasted image 20240322233307.png]]

### Erlang (Gamma) Noise Model:
$$
PDF = P(z) = \begin{cases}
\frac{a^bz^{b-1}}{(b-1)!}e^{-az} & z \ge 0 \\
0 & z < 0
\end{cases}
$$
- $\mu = \frac{b}{a}$
- $\sigma^2 = \frac{b}{a^2}$
- a & b are positive integer
- ![[Pasted image 20240322233733.png]]
- NO NEED TO REMEMBER VALUE OF 'K': NOT IN NOTES

### Exponential Noise Model:
$$
P(z) = \begin{cases}
ae^{-az} & z \ge 0 \\
0 & z \lt 0
\end{cases}
$$
- Special Case of Erlang (Gamma) Noise Model, where b = 1
- $\mu = \frac{1}{a}$
- $\sigma^2=\frac{1}{a^2}$
- ![[Pasted image 20240322234128.png]]

### Uniform Noise Model:
$$
P(z) = \begin{cases}
\frac{1}{b-a} & a \le z \le b \\
0 & otherwise
\end{cases}
$$
- $\mu = \frac{a+b}{2}$
- $\sigma^2=\frac{(b-a)^2}{12}$
- ![[Pasted image 20240322234414.png]]

### Salt-and-Pepper Noise Model:
$$
P(z) = \begin{cases}
P_a & \text{if z = a} \\
P_b & \text{if z = b} \\
0 & \text{otherwise}
\end{cases}
$$
- Conditions:
	1. If b > a -> graylevel 'b' appears as light dots and graylevel 'a' appears as dark dots
	2. If $P_a$ = 0 or $P_b$ = 0 the noise is uni-polar because it will be having only 1 probability
	3. If $P_a = P_b$ {approx. equal}, impulse will resemble salt & pepper granules
	4. For an 8-bit image, a = 0 (black) and b = 255 (white)
- ![[Pasted image 20240322234909.png]]

### One-Liners for Noises:
- Gaussian Noise arises due to electronic circuit, sensors, illumination, high temperature, etc.
- Rayleigh Noise is helpful in range imaging. It is specifically used in digital cameras
- Erlang and Exponential Noise are applicable in laser imaging
- Uniform noise are used in simulation for generating random noises
- Salt and Pepper noises appears when faulty switching takes place during imaging

### Periodic Noise:
- It arises from electrical or electro-mechanical interference during image acquisition
- It can be reduced by using frequency domain filtering

### Estimation of Periodic Noise Parameters:
- Fourier Spectrum Inspection
- Automated Analysis with knowledge of general location of frequency component
- Use data from image strip to calculate $\mu$ and $\sigma$ of graylevel, where, $$\begin{align}\displaylines{\mu & = \sum_{i=0}^{L-1}z_iP(z_i) \\ \sigma^2 & = \sum_{i=1}^{L-1}(z_i - \mu)^2P(z_i) \\ L & = 2^k (k \rightarrow bits)\\ L&=256\;\text{for 8-bit image} \\ z_i&=\text{Gray levels} \\ P(z_i)& = \text{Normalized Histogram Values}}\end{align}$$
