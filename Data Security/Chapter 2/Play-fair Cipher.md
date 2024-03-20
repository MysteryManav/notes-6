- It is an algorithm that is based on $5 \times 5$ matrix (key) of letters
- Matrix is constructed by filling in letters of keyword (minus duplicates) from left to right and from top to bottom, and then filling in the remainder of matrix with remaining letters in alphabetic order
- If matrix is of $5 \times 5$ then letters I and J can be counted as one letter

- **Encryption**:
	- Play-fair treats digrams (two letters) in plain-text as single units and translates these units into cipher-text digrams
	- Map each pair in key matrix
	- If letters appear on same row, replace letters to their immediate right respectively, wrapping to left side of row if necessary
	- If letters appear on same column, replace them with letters immediately below, wrapping around to top if necessary
	- If letters are on different rows and columns, replace them with letters on other corner of the same row. The order is important - The first letter of pair should be replaced first
