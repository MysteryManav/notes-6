### Periodic Noise Reduction:
- To remove the periodic noise, we use the frequency domain filtering, this filter removes the particular range of frequency from an image
- There are 3 types of filters for periodic noise reduction:
	1. Band Reject Filter
	2. Band Pass Filter
	3. Notch Filter
- **Band Reject Filter**:$$H(u, v) = \begin{cases}1; & D(u, v) < D_0 - \frac{w}{2} \\ \\0; & D_0 -\frac{w}{2} \le D(u, v) \le D_0 +\frac{w}{2} \\ \\1; & D(u, v) > D_0 + \frac{w}{2}\end{cases}$$
	- $D(u, v)$ => Distance from origin of centre frequency band
	- $w$ => Bandwidth
	- $D_0$ => Radial Centre (Cut-Off Frequency)
	- $D(u, v)$ => Region in original image where we perform B.R.F
	- **Butterworth Filter**:$$H(u, v) = \frac{1}{1 + \left[ \frac{D(u, v) \cdot w}{D^2(u, v) - D_0^2}\right]^{2n}}$$
		- $n$ = Order of Filter
	- **Gaussian Filter**:$$H(u, v) = 1 - e^{-\frac{1}{2}\left[ \frac{D^2(u, v) - D_0^2}{D(u, v) \cdot w}\right]}$$
- **Band Pass Filter**: Opposite Operation of B.R.F $$H_{b.p.}(u, v) = 1 - H_{b.r.}(u, v)$$
- **Notch Filters**: The notch filter passes the frequency in pre-defined neighbourhoods. The ideal notch reject filter transfer function of radius $D_0$, centre $(u_0, v_0)$, with symmetry at $(-u_0, -v_0)$, can be represented as:
$$
H(u, v) = \begin{cases}
0; & D_1(u, v) \le D_0 \;\;\&\;\;D_2(u, v)\le D_0 \\ \\
1; & \text{Otherwise}
\end{cases}
$$
$$
D_1(u, v) = \left[
\left(
u - \frac{M}{2} - u_0
\right)^2 +
\left(
v - \frac{N}{2} - v_0
\right)^2
\right]
^{\frac{1}{2}}
$$
$$
D_2(u, v) = \left[
\left(
u - \frac{M}{2} + u_0
\right)^2 +
\left(
v - \frac{N}{2} + v_0
\right)^2
\right]
^{\frac{1}{2}}
$$
- M and N are rows and columns of input image
- **Butterworth N.R.F**:$$H(u, v) = \frac{1}{1 + \left[ \frac{D^2}{D_1(u, v)D_2(u, v)} \right]^n}$$
- **Gaussian N.R.F**:$$H(u, v) = 1 - e^{-\frac{1}{2}\left[ \frac{D_1(u, v)D_2(u, v)}{D_0^2}\right]}$$
- **Notch Pass Filter**:$$H_{n.p.}(u, v) = 1 - H_{n.r.}(u, v)$$
