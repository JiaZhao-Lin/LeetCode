## Divide & Conquer

1. set the root val to the middle value. split the list in half and recursively set the value of sub tree
	```
	if len(nums) == 0:
			return
	mid_idx = len(nums) // 2
	left_node = self.sortedArrayToBST(nums[:mid_idx])
	right_node = self.sortedArrayToBST(nums[mid_idx+1:])
	```

1. get the mid node of a linked list. Slow node run at 1x speed, fast node 2x speed
	```
	def getMid(head):
		slow = head
		fast = head.next

		while fast and fast.next:
			slow = slow.next
			fast = fast.next.next

		return slow
	```

1. merging two linked list
	```
	def merge(list1, list2):
		newHead = tail = ListNode()

		while list1 and list2:
			if list1.val > list2.val:
				tail.next = list2
				list2 = list2.next
			else:
				tail.next = list1
				list1 = list1.next
			tail = tail.next

		if list1:
			tail.next = list1
		if list2:
			tail.next = list2

		return newHead.next
	```