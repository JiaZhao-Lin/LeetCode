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