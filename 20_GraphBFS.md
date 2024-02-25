1. 
```
while q:
	square, moves = q.popleft()
	for i in range(1, 7):
		nextSquare = square + i
		r, c = get_pos(nextSquare)
		if board[r][c] != -1:
			nextSquare = board[r][c]
		if nextSquare == end:
			return moves + 1
		if not nextSquare in visit:
			visit.add(nextSquare)
			q.append([nextSquare, moves+1])
```