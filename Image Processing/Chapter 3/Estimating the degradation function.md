- There are 3 methods to estimate the degradation function, if we have no knowledge about it:
	1. Estimation by Observation
	2. Estimation by Experimentation
	3. Estimation by Modelling
- **Estimation by Observation**: Let's suppose we are given a degraded image without any knowledge about the degradation function. Estimation by Observation can be  done using these steps:
	1. Identify good portion of image where the signal content is strong (High Contrast Area). Name it as $g_s(x, y)$. It's processed sub-image will be $\hat f_s(x, y)$
	2. Assuming noise $N(x, y)$ is eligible, we have:$$H_s(u, v) = \frac{G_s(u, v)}{F_s(u, v)}$$
	3. Apply inverse Fourier transform to the above equation and estimate the degradation function
- **Estimation by Experimentation**:
	1. Identify the device used for capturing the image and study the device settings
	2. Obtain impulse response of degradation by imaging a small white dot of light (impulse) using same device settings. The white dot must be as bright as possible to reduce the noise to negligible. The Fourier transform of an impulse is always constant. Therefore, we have:$$H(u, v) = \frac{G(u, v)}{A}$$ $A$ => Fourier transform of impulse
	3. Apply the inverse fourier transform to the above equation and estimate the degradation function
- **Estimate by Mathematical Modelling**: There are 3 possibilities:
	1. Complete Knowledge about the blur is known; Here, we apply inverse filtering (De-Convolution)
	2. Partial Knowledge about the blur is available; Here, we use 'Weiner' Filter
	3. No knowledge of the blur is available; We use blind convolution
