## Bit Manipulation

1. use `bin(num)[2:]` since bin value starting with "0b"
1. use a list to keep track of digits `l.append(str(carry % 2))` and ` ''.join(reversed(l)) `
1. pad with 0 to the left for 32 bits long
	- `f'{n:0>32}'`
	- `n.rjust(32,'0')`
