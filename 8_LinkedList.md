
## Linked List

1. use set to keep a record of the nodes visited
1. use carry to keep track of the number. keep track of the head with dummyHead, return dummyHead.next
	```
	digit1 = l1.val if l1 is not None else 0
	digit2 = l2.val if l2 is not None else 0

	carry += digit1 + digit2
	digit = carry % 10
	carry = carry // 10

	l1 = l1.next if l1 is not None else None
	l2 = l2.next if l2 is not None else None
	```

1. make maping between the copy and the original. first loop to initialize, second loop to link. use dict get() to get None and avoid KeyError

1. reverse node algo
	```
	cur = prev.next
	for _ in range(right - left):
		temp = cur.next
		cur.next = temp.next
		temp.next = prev.next
		prev.next = temp
	```

1. creating a mapping using the val of the node as the key and the node as the value. remove the appropriate node. 

1. zigzag pattern
	- create a mapping of row number and characters in that row
	```
	#	P   A   H   N
	#	A P L S I I G
	#	Y   I   R

	#HINT:
	#    P  A  Y  P  A  L  I  S  H  I  R  I  N  G
	#    -----------------------------------------
	#Row 1  2  3  2  1  2  3  2  1  2  3  2  1  2

	hashmap = defaultdict(str)
	irow = 1
	increment = 1

	for i in range(len(s)):
		hashmap[irow] += s[i]
		irow += increment
		if irow == numRows or irow == 1:
			increment *= -1
	```