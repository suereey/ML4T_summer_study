# 01-03: The power of Numpy
## Notes on notations
- Examples for array notation
![notation_01](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/screenshot/03_numpyarray_notation_01.PNG)
![notation_02](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/screenshot/03_numpyarray_notation_02.PNG)

## Creating Numpy arrays
- 1D array
- 2D array
- creat empty array with intial values
- creat empty array full of 1
- specify the data type in array: dtype
```
import numpy as np

def test_run():
	# List to 1D array
	print (np.array([2, 3, 4]))
	
	# List of tuples to 2D array
	print (np.array([(2, 3, 4), (5, 6, 7)]))
	
	# Empty array
	print (np.empty(5))
	print (np.empty((5,4)))
	print (np.empty((5,4,3)))
	
	# Array of 1s
	print (np.ones((5, 4)))
	
	# Specifying the datatype
	print (np.ones((5, 4), dtype=np.int_))
	
	
if __name__ == "__main__":
    test_run()
```

## Generating random numbers
### Sampling functions:
- numpy.random.random: Samples a Uniform distribution in [0.0, 1.0)

- numpy.random.rand: Like random, but slightly different syntax

- numpy.random.normal: Normal or Gaussian distribution

- numpy.random.randint: Integers from Uniform distribution


```
import numpy as np

def test_run():
	# Generate an array full of random numbers, uniformly samples from [0.0, 1.0)
	print (np.random.random((5, 4))) # pass in a size tuple
	
	# Generate an array full of random numbers, uniformly samples from [0.0, 1.0)
	print (np.random.rand(5, 4)) # function arguments (not a tuple)
	
	# Sample numbers from a Gaussian (normal) distribution
	print (np.random.normal(size=(2, 3))) # "standard normal" (mean = 0, s.d. = 1)
	
	# Sample numbers from a Gaussian (normal) distribution
	print (np.random.normal(50, 10, size=(2, 3))) # change mean to 50 and s.d. to 10
	
	# Random integers
	print (np.random.randint(1)) # a single integer in [0, 10)
	print (np.random.randint(0, 10)) # same as above, specifying [low, high) explicit
	print (np.random.randint(0, 10, size=5)) # 5 random integers as a 1D array
	print (np.random.randint(0, 10, size=(2, 3))) # 2x3 array of random integers
	
if __name__ == "__main__":
    test_run()

```

## Array attributes
- shape, size, dimenssion...

```
	a = np.random.random((5, 4))  # 5x4 array of random numbers
	print (a)   # will return the whole arrray
	print (a.shape) # will return (5,4). 5: # of row; 4: # of columns.
	
	print (a.shape[0])  # number of rows
	print (a.shape[1])  # number of columns
	
	print (len(a.shape)) # will return the dimenssion, 2
	print (a.size)       # will return the size, 20   
	print (a.dtype)
```

## Operations on arrays
- sum (sum all, sum rows, sum columns)
- max, min, mean...
```
    np.random.seed(693)  # seed the random number generator
	a = np.random.randint(0, 10, size=(5, 4)) # 5x4 random integers in [0, 10)
	print ("Array:\n", a)
	
	# Sum of all elements
	print ("Sum of all elements:", a.sum())
	
	# Iterate over rows, to compute sum of each columns
	print ("Sum of each column:\n", a.sum(axis=0))
	
	# Iterate over columns to compute sume of each rows
	print ("Sum of each row:\n", a.sum(axis=1))
	
	# Statistics: min, max, mean (across rows, cols, and overall)
	print ("Minimum of each colulmn:\n", a.min(axis=0))
	print ("Maximum of each row:\n", a.max(axis=1))
	print ("Mean of all elements:", a.mean()) # leave out axis arg.
```
## Locate maximum value in an array
- find max value: array.max()
- find max value's index: np.argmax(array)
```
def get_max_index(a):
    """Return the index of the maximum value in given 1D array."""
    return np.argmax(a)

def test_run():
    a = np.array([9, 6, 2, 3, 12, 14, 7, 10], dtype=np.int32)  # 32-bit integer array
    print( "Array:", a)
    
    # Find the maximum and its index in array
    print ("Maximum value:", a.max())
    print ("Index of max.:", get_max_index(a))
```

## Time python operations
- Find time: time()
- numpy is fast
```
import numpy as np
import time	
	
def test_run():
	t1 = time.time()
	print ("ML4T")
	t2 = time.time()
	print ("The time taken by print statement is ", t2 - t1, " seconds")
```

- Sample code that shows numpy is fast
```
import numpy as np
from time import time


def how_long(func, *args):
	"""Execute function with given arguments, and measure execution time."""
	t0 = time()
	result = func(*args) # all argument are passed in as-is
	t1 = time()
	return result, t1 - t0

def manual_mean(arr):
	"""Compute mean (average) of all elements in the given 2D array."""
	sum = 0
	for i in range(0, arr.shape[0]):
		for j in range(0, arr.shape[1]):
			sum = sum + arr[i, j]
	return sum / arr.size

def numpy_mean(arr):
	"""Compute mean(average) using Numpy"""
	return arr.mean()

def test_run():
	"""Function called by Test Run."""
	nd1 = np.random.random((1000, 10000)) # use a sufficiently large array

	# Time the two functions, retrieving results and execution times
	res_manual, t_manual = how_long(manual_mean, nd1)
	res_numpy, t_numpy = how_long(numpy_mean, nd1)
	print ("Manual: {:.6f} ({:.3f} secs.) vs. Numpy: {:.6f} ({:.3f} secs.)".format(res_manual, t_manual, res_numpy, t_numpy))

	# Make sure both give us the same answer (upto some precision)
	assert abs(res_manual - res_numpy) <= 10e-6, "Results aren't equal!"

	# Compute speedup
	speedup = t_manual / t_numpy
	print ("Numpy mean is", speedup, "times faster than manual for loops.")


if __name__ == "__main__":
    test_run()
```

## Accessing array element: row, column
- select element: 
    - element at a position: a[3, 2]
    - element in defined range: a[0:1, 1:3]
- Assign value: 
    - element at a position: a[0, 0] = 1
    - element in defined range, 1 value: a[0,:] = 2
    - element in defined range, multi values: a[:, 3] = [1, 2, 3, 4, 5]
```
def test_run():
    a = np.random.rand(5, 4)
    print ("array:\n", a)

    # Accessing element at position (3, 2), (4th row, 3rd column)
    element = a[3, 2]
    print (element)

    # Element in defined range
    print (a[0, 1:3])

    # Top-left corner
    print (a[0:2, 0:2])

    # Slicing
    # Note: Slice n:m:t specifies a range that starts n, and stops before m, in
    print( a[:, 0:3:2]) # will select columns 0, 2 for every row

    # Assigning a value to a particular location
    a[0, 0] = 1
    print ("\nModified (replaced one element):\n", a)

    # Assigning a single value to an entire row
    a[0,:] = 2
    print ("\nModified (replaced a row with a single value):\n", a)

    # Assigning a list to a column in an array
    a[:, 3] = [1, 2, 3, 4, 5]
    print ("\nModified (replaced a column with a list):\n", a)

```
## Index an aray with another array
```
    a = np.random.rand(5)
	# if the result return [0.1, 0.2, 0.5, 0.7, 0.9]
	
    # accessing using list of indices
	indices = np.array([1,1,2,3])

	print (a[indices])  
    # it will return [0.1, 0.1, 0.2, 0.5] as correponding to 1, 1, 2, 3
```

## Boolean or "mask" index arrays
- mask the value:
    - keep data < mean value: a[a<mean]
    - replace data < mean value by mean value: a[a<mean] = mean
    - The expression a < mean produces a boolean array, like:
[[False, False, True, False, False, False, True, True, True],
 [True, True, False, False, True, True, False, True, True]]
- NumPy Reference: [Indexing](https://numpy.org/doc/stable/reference/arrays.indexing.html) 
    - [Integer array indexing](https://numpy.org/doc/stable/reference/arrays.indexing.html#integer-array-indexing)
    - [Boolean array indexing](https://numpy.org/doc/stable/reference/arrays.indexing.html#boolean-array-indexing)
```
    a = np.array([(20,25,10,23,26,32,10,5,0),(0,2,50,20,0,1,28,5,0)])
	print (a)
	
	# calculating mean
	mean = a.mean()
	print (mean)
	
	# masking
	print (a[a<mean])
	
	# masking2
	a[a<mean]= mean
	print (a)
```

## Arithmetic operations
```
    # Multiple a by 2
	print ("\nMultiply a by 2:\n", 2 * a)
	
	# Divide a by 2
	print ("\nDivide a by 2:\n", a / 2)
	
	# Divide a by 2.0 to float
	print ("\nDivide a by 2:\n", a / 2.0)
	
	b = np.array([(100, 200, 300, 400, 500), (1, 2, 3, 4, 5)])
	print ("\nOriginal array b:\n", b)
	
	# Add the two arrays
	print ("\nAdd a + b:\n", a + b)
	
	# Multiply a and b
	print ("\nMultiply a and b:\n", a * b)
	
	# Divide a by b
	print ("\nDivide a by b:\n", a / b)
```