# Python

## List
1. `append(x)`: Adds an element `x` to the end of the list.
1. `extend(iterable)`: Adds all elements of an iterable (e.g., list, tuple) to the end of the list.
1. `insert(i, x)`: Inserts an element `x` at position `i` in the list.
1. `remove(x)`: Removes the first occurrence of element `x` from the list.
1. `pop(i)`: Removes and returns the element at position `i` from the list (default: last element).
1. `index(x)`: Returns the first index of element `x` in the list.
1. `count(x)`: Returns the number of times element `x` appears in the list.
1. `sort()`: Sorts the list in ascending order.
1. `reverse()`: Reverses the order of elements in the list.
1. `copy()`: Returns a shallow copy of the list.

### Tricks
```
sorted(l, reverse=True)	# not inplace sort
sorted(l, key=len, reverse=True)
l.sort()	# inplace sort

l[2:5] = [20, 30]	# slice replacement, iterable only
del l[2:5]	# slice deletion

l = np.array([1, 2, 3, 4, 5])
l[ l>2 ]	# masking: l[[False, False, True, True, True]] = [3, 4, 5]
l[ [3, 4] ]	# index selection: [4, 5]
l[ [3, 4] ] = 0	# index selection replacement: [1, 2, 0, 4, 0]
```

## String
### Methods
1. `split(sep)`: Splits the string into a list of substrings based on the separator `sep`.
1. `replace(old, new)`: Replaces all occurrences of substring `old` with `new` in the string.
1. `find(substring)`: Returns the first index of the substring in the string (or -1 if not found).
1. `count(substring)`: Counts the number of occurrences of the substring in the string.
1. `index()`: Searches the string for a specified value and returns the position of where it was found.
1. `join(iterable)`: Joins a sequence of strings with the given separator.
1. `capitalize()`: Converts the first character of the string to uppercase.
1. `lower()`: Converts all characters in the string to lowercase.
1. `upper()`: Converts all characters in the string to uppercase.
1. `strip()`: Removes leading and trailing whitespaces from the string.
1. `isalnum()`: Returns True if all characters in the string are alphanumeric.
1. `isalpha()`: Returns True if all characters in the string are in the alphabet.
1. `isdigit()`: Returns True if all characters in the string are digits.
1. `startswith(prefix)`: Checks if the string starts with the given `prefix`.
1. `endswith(suffix)`: Checks if the string ends with the given `suffix`.

## collections
1. `collections.Counter`: elements: dictionary keys. counts: dictionary vals
	- `collections.Counter('aab')`
	- `Counter({'a': 2, 'b': 1})`
	- `most_common(n)`: Return a list of the n most common elements and their counts from the most common to the least.
	- `keys()`
	- `values()`
	- `items()`
1. `collections.defaultdict`: provide default values for the key that does not exist and never raises a KeyError
	- `collections.defaultdict(list)`
1. `collections.namedtuple`: simple, lightweight data structures similar to a class, but without the overhead of defining a full class
	- `Student = namedtuple('Student', ['name', 'age', 'DOB'])`
	- `S = Student('James', '20', '2000')`
	- `print(S.name)`

## random
1. `random.randint(a, b)`: Return a random integer N such that a <= N <= b
1. `random.randrange(start, stop[, step])`: Return a randomly selected element from range(start, stop, step).
1. `random.choice(seq)`: Return a random element from the non-empty sequence seq. 
1. `random.shuffle(x)`: Shuffle the sequence x in place.
1. `random.uniform(a, b)`: Return a random floating point number N such that a <= N <= b for a <= b and b <= N <= a for b < a



