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
1. the main idea is that when iterating over the intervals there are three cases:
	- the new interval is in the range of the other interval
	- the new interval's range is before the other
	- the new interval is after the range of other interval
	```
	for interval in intervals:
		if interval[1] < newInterval[0]:
			result.append(interval)
		elif interval[0] > newInterval[1]:
			result.append(newInterval)
			newInterval = interval
		elif interval[1] >= newInterval[0] or interval[0] <= newInterval[1]:
			newInterval[0] = min(interval[0], newInterval[0])
			newInterval[1] = max(newInterval[1], interval[1])
	result.append(newInterval); 
	```