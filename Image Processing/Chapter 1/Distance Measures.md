
### Distance Measures:
- Distance between pixels p, q and z with co-ordinates $(x, y) , (s, t), (v, w)$ respectively is given by:
	1. $D(p, q) \ge 0;\;\text{[D(p, q) = 0 if p = q]}$ is called reflexivity
	2. $D(p, q) = D(q, p)$ is called symmetry
	3. $D(p, z) \le D(p, q) + D(p, z)$ is called transitivity
  where D is distance

### Euclidean Distance:
- Euclidean Distance between 'p' and 'q' is defined as: $$D_e(p, q)=\sqrt{[(x - s)^2 + (y - t)^2]}$$
### City Block Distance: 
- The $D_4$ distance between p and q is defined as: $$D(p, q)=\lvert x - s\rvert + \lvert y - t\rvert$$ In this case, pixels having $D_4$ distance from $(x, y)$ less than or equal to some values 'r' form a diamond centred at $(x, y)$)
- It is the distance between a pixel and its $N_4$ neighbours

### Chess Board Distance:
- The $D_8$ distance between p and q is defined as: $$D_8(p, q) = max(\lvert x - s \rvert, \lvert y - t\rvert)$$
- It is the distance between pixel and its $N_8$ neighbours
