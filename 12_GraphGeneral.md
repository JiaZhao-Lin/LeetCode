## Graph General

1. if we find a target we remove all it's neibors recursively
1. start from the boarder
	- replace all O and their neighboring O to N
	- replace all O to X
	- replace all N to O
1. A hash map to keep track of already visited and already cloned nodes
    - If a neighbor is already cloned and visited, we just append it to the current clone neighbors list, otherwise, we dfs clone it first and append it