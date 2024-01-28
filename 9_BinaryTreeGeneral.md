## Binary Tree General

1. Recursion: handling None case first, then recursively do work
	```
	if root == None:
			return 0
	return max(self.maxDepth(root.left), self.maxDepth(root.right)) + 1
	```
1. Recursion: 
	- is: test object identity
	- =: test values
	```
	if p and q:
		return p.val == q.val and self.isSameTree(p.left, q.left) and self.isSameTree(p.right, q.right)
	return p is q
	```
1. Recursion: swaping l and r nodes

1. Recursion: symmetry check
	```
	def isSame(left, right):
		if left == None and right == None:
			return True
		if left == None or right == None:
			return False
		if left.val != right.val:
			return False
		
		return isSame(left.left, right.right) and isSame(left.right, right.left)
	```

1. Tree traversal
	- Preorder: Root-Left-Right
	- Inorder: Left-Root-Right
	- Postorder: Left-Right-Root
1. Binary Tree from Preorder and Inorder Traversal
	```
	index = inorder.index(preorder.pop(0))
	root = TreeNode(inorder[index])
	root.left = self.buildTree(preorder, inorder[:index])
	root.right = self.buildTree(preorder, inorder[index+1:])
	```
1. Binary Tree from Inorder and Postorder Traversal
	```
	index = inorder.index(postorder[-1])
	root = TreeNode(postorder[-1])
	root.left = self.buildTree(inorder[:index], postorder[:index])
	root.right = self.buildTree(inorder[index+1:], postorder[index:-1])
	```

1. BFS, for each node, we pack it and a number labeling the current level to tuple
	- check if the current node is in the same level as the previous node

1. recursively substract the node value from the target value 
	- stop when both children are None, check if current target value is node value

1. 
	```
	if(root == None):
		return 0
	return( self.countNodes(root.left) + self.countNodes(root.right) + 1 )
	```

1. DFS binary tree and append the node into a list. The node in the list is sorted since it's from a binary tree. Relink the node in the list

1. Define a DFS function that take in the sum up until the node, return if both leaf are None, return 0 if current node is None.