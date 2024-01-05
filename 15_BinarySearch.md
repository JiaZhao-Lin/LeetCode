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