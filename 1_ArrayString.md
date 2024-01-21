## Ideas

1. Start from the either end and fill the list. Stop when the second list is all inserted into the first.

1. Keep a write index. increment it when the requirement is met. 

1. Two pointers to keep track

1. Keep track of min price and max profit seen. 

1. Break every trade down to several overnigt trades. COLLECT EVERY POSSIBLE GAINS!

1. Check maximumn reach within the available step. only jump when we absolutely have to

1. Find the first index where citation is smaller than or equal to sorted array index

1. when dealing with special cases, convert them to known case such as: replace("IV", "IIII")
1. use zip or zip_longest to unpack

1. calculate prefix_product * postfix_product for each element
	```
	for i in range(n):
		result[i] = prefix_product
		prefix_product *= nums[i]
	for i in reversed(range(n)):
		result[i] *= postfix_product
		postfix_product *= nums[i]
	```
	
1. exploit the fact there must be one solution
	```
	if (sum(gas) - sum(cost) < 0):
		return -1
	
	gas_tank, start_index = 0, 0
	
	for i in range(len(gas)):
		gas_tank += gas[i] - cost[i]
		
		if gas_tank < 0:
			start_index = i+1
			gas_tank = 0
		
	return start_index
	```

1. Creating Dictionary for Lookup, including all outlier
	```
	r = ''
	for n in reversed(sorted(num_map.keys())):
		while n <= num:
			r += num_map[n]
			num-=n
	return r
	```
