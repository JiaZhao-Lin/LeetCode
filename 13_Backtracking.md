## Backtracking

1. Given a string containing digits from 2-9 inclusive, return all possible letter combinations that the number could represent.
	```
	ans = ['']
	for d in digits:
		new_ans = [x+y for x in ans for y in key_map[d]]
		ans = new_ans
	return ans
	```
	```
	res = []
	def backtrack(combination, next_digits):
		if not next_digits:
			res.append(combination)
			return
		
		for letter in phone[next_digits[0]]:
			backtrack(combination + letter, next_digits[1:])
	```

1. Given two integers n and k, return all possible combinations of k numbers chosen from the range [1, n].
	```
	ans = []
	def backtrack(comb, start, count):
		if not count:
			ans.append(comb)
			return
		
		for i in range(start, n+1):
			out = list(comb)
			out.append(i)
			backtrack(out, i+1, count-1)
			
		return
	
	backtrack([], 1, k)
	```

1. Return all the possible permutations
	```
	def backdrop(permu, nums):
		if len(nums) == 0:
			ans.append(permu)
			return

		for i in range(len(nums)):
			permu_ = list(permu)
			permu_.append(nums[i])
			nums_next = nums[:i] + nums[i+1:]
			backdrop(permu_, nums_next)
	```

1. keep current combination, current combination sum, current index (to avoid repeats)
	```
	def dfs( l, curr_sum, idx ):
	if curr_sum > target:
		return
	if curr_sum == target:
		ans.append(l)
		return

	for i in range(idx, n):

		dfs(l + [candidates[i]], curr_sum + candidates[i], i)

	return
	```

1. Given a str, we can either add '(' or ')' to it
	- It's always valid to add '(' it's fewer than n
	- It's only valid to add ')' when there are more '(' in the string
	```
	def dfs(l, r, s):
		if len(s) == n * 2:
			ans.append(s)
			return

		if l < n:
			dfs(l + 1, r, s+'(')

		if r < l:
			dfs(l, r + 1, s+')')
	```