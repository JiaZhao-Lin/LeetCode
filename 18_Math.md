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

1. all trailing 0 is from factors 5 * 2. just count how many 5 factors in all number from 1 to n.
	```
	return 0 if n == 0 else n / 5 + self.trailingZeroes(n / 5)
	```
