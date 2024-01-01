## Matrix

1. use tuple encoding the row/column number
	- add tuple encoded element to a list
	- if there are repetition, the len of set will not equal to len of the list
1. rotate the remaining matrix
	- pop row
	- rotate: ( list( zip( *matrix ) ) )[::-1]
	- repeat