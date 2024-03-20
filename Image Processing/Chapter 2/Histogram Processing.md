
![[Histogram.excalidraw]]

- In image processing, histogram is the occurrence of various graylevels. It is used for manipulating contrast and brightness. Image quality can be controlled by normalising histogram
- Two types of numerical:
	1. Histogram Stretching (Scaling)
	2. Histogram Equalisation

### Histogram Stretching:
$$
T = \frac {S_{max} - S_{min}}{r_{max} - r_{min}} \cdot (r - r_{min})\quad+\quad S_{min}
$$

### Histogram Equalisation:
- We can represent an image like the matrix below, where no. of times a pixel has occurred is its frequency count

| 4   | 4   | 4   | 4   | 4   |
| --- | --- | --- | --- | --- |
| 3   | 4   | 5   | 4   | 3   |
| 3   | 5   | 5   | 5   | 3   |
| 3   | 4   | 5   | 4   | 3   |
| 4   | 4   | 4   | 4   | 4   |

### Histogram Specification (Matching):
- It is similar to Histogram Equalisation with the following changes:
	1. Used to equalise the graylevels of an image with respect to another image
	2. Has an additional "Mapping" step where the graylevels of pixels are changed to modify the distribution of graylevels and equalise the image with respect to another