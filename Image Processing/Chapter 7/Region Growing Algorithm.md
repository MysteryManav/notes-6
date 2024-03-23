- Region Growing is a procedure that groups pixels or sub-regions into larger regions based on the principle of similarity
- The principle of similarity states that: "A region is coherent if all the pixels of that region are homogeneous"
- Homogeneity may be with respect to graylevel, colour, texture, shape, etc.
- Steps:
	1. Select Seed points, there may be single or multiple seed points
	2. Select a threshold value 'T' {It can be anything like average of seed points, etc.}
	3. Use the following formula and find the possible values for seed values:$$\lvert f(x, y) - f(x', y') \rvert \le T$$
	4. Draw the regions
