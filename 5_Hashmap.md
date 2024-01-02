## Hashmap

1. all(ransomNote.count(c) <= magazine.count(c) for c in set(ransomNote))
1. using set to record mapping
	- zipped_set = set(zip(s, t))
	- len(zipped_set) == len(set(s)) == len(set(t))
1. using Counter: Counter(s) == Counter(t)
1. using map to store all value and its index