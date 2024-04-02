- It is also known as Reverse Filtering
- Inverse Filtering in Image Processing is done to remove the blur and noise available so that we can restore the image with higher accuracy compared to the original one
- We know $G(u, v) = H(u, v) \cdot F(u, v) + N(u, v)$, to obtain, $F(u, v)$, we can write $$F(u, v) = \frac{G(u, v)}{H(u, v)} - \frac{N(u, v)}{H(u, v)}$$
- If noise is zero, and we have full knowledge about the blur or degradation, we directly use *"De-Convolution"* to obtain $F(u, v)$ (un-degraded image)
- If noise is present, and $H(u, v) \approx 0$, this means $N(u, v) \approx \infty$. Hence, inverse filtering is not a good choice for un-degraded image. Therefore, we will use *'Wiener'* Filter

### Wiener Filter:
- It gives estimation of original uncorrupted image
- It removes additive noise and inverse the blurring simultaneously
- The wiener filter tries to minimise the estimated error between the original image *f* and the corrected image $\hat f$
- Assumptions to be made for Wiener filter:
	1. The noise and image are not correlated
	2. Either the blurring $H(u, v)$ or the noise should have a minimum value for the Wiener filter to act properly
	3. The grey levels in the estimate are linear function of degraded image
- $$e = E\{(f - \hat f)^2\}$$ e => Least Mean Square Error
