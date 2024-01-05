## Math

1. 	```
	for i in reversed(range(len(digits))):
		if digits[i] < 9:
			digits[i] += 1
			return digits
		digits[i] = 0
	```