- It refers to image plane itself, based on direct manipulation of pixels in an image
- Spatial Processing (Domain):
	1. *Intensity Transformation*:
		- For contrast manipulation and individual thresholding
		- Works on individual pixels
	2. Spatial Filtering:
		- Works on neighbourhood of pixels
		- For image sharpening
- They are:
	1. Computationally Efficient
	2. Require less processing resources
- Denoted by:$$g(x, y)=T[f(x, y)]$$ where, $$\displaylines{f(x, y) \rightarrow \text{input}\\ g(x, y) \rightarrow \text{processed image}\\ T \rightarrow \text{operator on f over same neighbourhood}}$$
- Simplest for of $T$ is for neighbourhood of size $|X|$ $$S=T(r)$$ where, $r$ and $s$ representing gray level of $f(x, y)$ and $g(x, y)$ at any point $(x, y)$. $T$ becomes a gray level transformation

### Types of Spatial Domain
- **Point Operation**: Modifying every pixel by equation that is not dependent on other pixel values $$g(m, n)=T[f(m, n)]$$ ![[Point Operation]]
- **Mask Operation**

![[Mask Operation.excalidraw]]

- **Global Operation**

![[Global.excalidraw]]
