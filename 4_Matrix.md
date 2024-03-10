## Matrix

1. use tuple encoding the row/column number
	- add tuple encoded element to a list
	- if there are repetition, the len of set will not equal to len of the list
1. rotate the remaining matrix
	- pop row
	- rotate: ( list( zip( *matrix ) ) )[::-1]
	- repeat

1. Two passes through the matrix
	- Remember the row and column numbers of all 0 in a single list
	- Set entire row to 0 and then loop over the columns