- It is used to construct or recover an image that has been degraded using prior knowledge of degradation phenomena
- Restoration techniques are used for modelling the degradation and applying inverse process to recover original image
- There are 2 types of spatial techniques:
	1. Spatial domain for additive noise
	2. Frequency domain for image blurring

![[Restoration Steps.excalidraw]]

### Mathematical Representation of Degradation:
- In Spatial Domain:$$g(x, y) = h(x, y)*f(x, y) + n(x, y)$$
- In Frequency Domain: Convolution becomes product:$$G(u, v) = H(u, v) \times f(u, v) + N(u, v)$$
