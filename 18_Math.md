## Math

1. 	```
	for i in reversed(range(len(digits))):
		if digits[i] < 9:
			digits[i] += 1
			return digits
		digits[i] = 0
	```

1. use binary search to find the sqrt(x)
	```
	left, right = 1, x
	while left <= right:
		mid = (left + right)//2
		mid_sq = mid * mid
		if mid_sq == x:
			return mid
		if mid_sq > x:
			right = mid - 1
		else:
			left = mid + 1
	return right
	```