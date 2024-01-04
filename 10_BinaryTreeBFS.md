## Binary Tree BFS
```
queue = []
queue.append(s)
visited = [] # List to keep track of visited nodes.

while queue:
	s = queue.pop(0)
	for i in self.graph[s]:
		if visited[i] == False:
			queue.append(i)
			visited[i] = True
```

1. keep track of the level in the tree with tuple (level, val)
	- only append one value in each level
	```
	ans =[]
	def dfs(node =root,level=1):
		if not node: return
		
		if len(ans) < level: 
			ans.append(node.val)
		dfs(node.right,level+1)         #  <--- right first
		dfs(node.left ,level+1)         #  <--- then left

		return 
	```