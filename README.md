# np.c_ vs zip()

The difference is that np.c_ will concatenate along columns and give out df, whereas zip will concatenate along columns and give out tuple

here's an example to demonstrate the difference between np.c_ and the zip() method:

```python
import numpy as np

# Example arrays
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
c = np.array([7, 8, 9])
d = np.array([10, 11, 12])

# Using np.c_ to concatenate arrays
concatenated_array = np.c_[a, b, c, d]
print(concatenated_array)

# Using zip() to concatenate arrays
zipped_array = list(zip(a, b, c, d))
print(zipped_array)
```

Output:

```python
[[ 1  4  7 10]
 [ 2  5  8 11]
 [ 3  6  9 12]]
[(1, 4, 7, 10), (2, 5, 8, 11), (3, 6, 9, 12)]

```
