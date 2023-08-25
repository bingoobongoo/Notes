A **Fenwick Tree** (also called Binary Indexed Tree) is a [[Data Structures|data structure]] that supports sum range queries as well as setting values in a static array and getting the value of the prefix sum up some index efficiently.

Unlike a regular array, in a Fenwick Tree a specific cell is responsible for other cells as well. The position of the **least significant bit (LSB)** determines the range of responsibilities that cell has to the cells below itself.  All odd numbers have their first least significant bit set in the ones position, so they are only responsible for themselves.

![[Pasted image 20230725213046.png]]

## Range Query Algorithm

```python
def prefixSum(self, i):
	sum = 0
	while i != 0:
		sum += tree[i]
		i -= LSB(i)
	return sum

def rangeQuery(self, i, j):
	return prefixSum(j) - prefixSum(i)
```

Where **LSB** returns the value of the least significant bit.
 
## [[Big-O Notation|Complexity]]

| Operation | Complexity |
| --- | --- |
| Construction | $O(n)$ |
| Point Update | $O(\log n)$ |
| Range Sum | $O(\log n)$ |
| Range Update | $O(\log n)$ |
| Adding Index | N/A |
| Removing Index | N/A |

 