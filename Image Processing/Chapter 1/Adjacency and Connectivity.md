- **Adjacency**: Two pixels are adjacent if they are neighbours and their intensity level 'V' satisfy some specific criteria of similarity
	*Eg*: 
		V = {1}
		V = {0, 2}
		Binary Image = {0, 1}
		Grayscale Image = {0, 1, 2, ...., 255}

### Three types of Adjacency:
- 4-adjacency
- 8-adjacency
- m-adjacency

### 4-Adjacency:
- Two pixels 'p' and 'q' with values from set 'V' are 4-adjacent if 'q' is in set of $N_4(p)$

### 8-Adjacency:
- Two pixels 'p' and 'q' with values from set 'V' are 8-adjacent if q is in set of $N_8(p)$

### m-Adjacency:
- Two pixels 'p' and 'q' with values from set 'V' are m-adjacent if:
	1. q is in $N_4(p)$
			OR
	2. q is in $N_D(p)$ and the set $N_4(p)\;\bigcap\;N_4(q)$ have no pixels whose values are from 'V'

### Connectivity:
- Two pixels are said to be connected if their exists a path between them
- Let 's' represent subset of pixels in an image
- Two pixels 'p' and 'q' are said to be connected in 'S' if their exists a path between them consisting entirety of pixels in 'S'

### Paths:
- A path from pixel 'p' with co-ordinate (x, y) with pixel 'q' with co-ordinates (s, t) is a sequence of distinct sequence with co-ordinates $(x_0, y_0)$, $(x, y)$, ...., $(x_n, y_n)$ where $$\displaylines{(x, y) = (x_0, y_0) \\(s, t) = (x_n, y_n)}$$
- *Closed Path*: $(x_0, y_0) = (x_n, y_n)$
