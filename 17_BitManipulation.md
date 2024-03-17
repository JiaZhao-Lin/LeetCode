## Bit Manipulation

1. use `bin(num)[2:]` since bin value starting with "0b"
1. use a list to keep track of digits `l.append(str(carry % 2))` and ` ''.join(reversed(l)) `
1. pad with 0 to the left for 32 bits long
	- `f'{n:0>32}'`
	- `n.rjust(32,'0')`

1. XOR of any two num gives the difference of bit as 1 and same bit as 0
	1 ^ 1 == 0 because same numbers have same bits. 
    ```
	xor = 0
	for num in nums:
		xor ^= num
	return xor
	```

1. `( ( 3*sum((set(nums))) ) - sum(nums) ) // 2`
        