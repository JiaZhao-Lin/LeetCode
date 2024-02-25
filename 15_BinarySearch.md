## Binary Search

```
left, right = 0, len(nums)
while left < right:
	mid = (left + right) // 2
	if target > nums[mid]:
		left = mid + 1
	else:
		right = mid
return left
```

1. `any(target in row for row in matrix)`
1. find peak element 
	```
	# if the mid index is not the peak, then the array must be ascending to the right of the mid
	while left < right:
		mid = (left + right) // 2
		if nums[mid] > nums[mid+1]:
			right = mid
		else:
			left = mid + 1
			
	return left
	```

1. apply binary search by determining which half of our array is sorted and whether the target lies within it.

1. 
	- if target exists, returns the leftmost idx of target.
    - If target doesn't exist, returns the leftmost idx of some num > target.
	- If target doesn't exist and target > all nums, returns len(nums)
	search the (target+1): it always give 1 index higher if the target exist
	```
	low = search(target)
    high = search(target+1)-1
	```