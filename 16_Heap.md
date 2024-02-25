## Heap

1. Heaps are binary trees for which every parent node has a value less than or equal to any of its children.

1. use heapq.heappush(minHeap, num) to push num into list
1. use heapq.heappushpop(minHeap, num) to push num and pop smallest num from the list

1. use BFS to visit each position. travases the 
	```
	heap=[]
	heapq.heappush(heap,(nums1[0]+nums2[0],0,0))
	visited=set()
	visited.add((0,0))
	output=[]
	while len(output)<k and heap:
		val=heapq.heappop(heap)
		i, j = val[1], val[2]
		output.append([nums1[i],nums2[j]])

		if(i+1<len(nums1) and (i+1,j) not in visited):
		if(j+1<len(nums2) and (i,j+1) not in visited):
	```