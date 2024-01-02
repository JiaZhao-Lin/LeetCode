## Intervals

1. modifying a list record while looping
	```
	if ranges and ranges[-1][1] == n-1:
		ranges[-1][1] = n
	else:
		ranges.append([n, n])
	```
	```
	if not merged or merged[-1][-1] < i[0]:
		merged.append(i)
	else:
		merged[-1][-1] = max(merged[-1][-1], i[-1])
	```
1. 