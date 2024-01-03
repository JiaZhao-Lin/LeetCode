
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