- Segmentation refers to the process of partitioning an image into multiple regions and extract meaningful region known as *Region of Interest* (R.O.I)
- R.O.I varies with application. No single algorithm exist for segmenting R.O.I
- An image can be partitioned into regions $R_1, R_2, \dots, R_n$. Let *R* be the entire image region and segmentation is partitioning R into *m* subgroups of $R_i$. The properties of regions are:
	1. $$\sum_{i=1}^nR_i = R$$
	2. $R_i$ should be connected region, not open ended
	3. $R_i \bigcap R_j = \phi$ (null), i.e., they must not share any common properties
	4. $P(R_i) = \text{TRUE}$; for i = 1, 2, 3, ...., n, where, 'P' is the predicate. Predicate means property of the image (colour, grayscale, etc.)
	5. $P(R_i \bigcup R_j) = \text{FALSE}$; for $i\neq j$; which means that no characteristics must be union of 2 different segment images
