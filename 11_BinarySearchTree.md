## Binary Search Tree

1. retriving all value in the binary search tree
	```
	def inorder(self, root, output):
		if root == None:
			return
		else:
			self.inorder(root.left, output)
			output.append(root.val)
			self.inorder(root.right, output)
	```
	- only comparing neighboring element to get the min

