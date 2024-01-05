## Divide & Conquer

1. set the root val to the middle value. split the list in half and recursively set the value of sub tree
	```
	if len(nums) == 0:
			return
	mid_idx = len(nums) // 2
	left_node = self.sortedArrayToBST(nums[:mid_idx])
	right_node = self.sortedArrayToBST(nums[mid_idx+1:])
	```
