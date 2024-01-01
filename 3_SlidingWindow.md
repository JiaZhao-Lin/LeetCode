## Sliding Window

1. two pointer l and r
	- slide r until the sum is greater than the target
	- slide l when the sum is small than the target
	- for r in range(len(nums)): add r value, sub l value, compare min length with previous min length
1. use dictionary to store the elem as the key, the last appear index has been seen so far as value
	- update seen each iteration
	- update output max length after seeing a new character
	- if s[r] is not inside the current window, keep increase the r
	- is inside the current window, change the window by moving l to seen[s[r]] + 1
