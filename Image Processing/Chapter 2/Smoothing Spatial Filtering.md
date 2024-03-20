- They are used to reduce noises from an image or blurring. There are 2 types of smoothing spatial filters:
	1. Linear Filters
	2. Non-Linear (Order Statistics Filter)

### Linear Filters:
- They are simply the average of the pixels contained in the neighbourhood of the filter mask. The idea is replacing the value of every pixel in an image by the average of the graylevels in the neighbourhood defined by the filter mask
- Types of Linear Filters:
	1. Averaging Filters
	2. Weighted Averaging Filters
- Sometimes also known as Low-Pass filters

### Order Statistics Filter:
- They are also known as order statistics filters. There are 3 types of non-linear filters:
	1. Median Filter
	2. Min Filter
	3. Max Filter
- There are no individual masks for non-linear filters. The non-linear filters have excellent noise reduction capabilities with less blurring. They are also effective for salt and pepper noise removal
- Near 0: Pepper Noise
- Near 255: Salt Noise
