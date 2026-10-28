NumPy Basics – Python Practice Notes

1. What is NumPy?

NumPy is a Python library used for numerical calculations and working with arrays.

Import NumPy before using it:

import numpy as np

2. Python List vs NumPy Array

Python list

numbers = [10, 20, 30, 40]
print(numbers * 2)

Output:

[10, 20, 30, 40, 10, 20, 30, 40]

Multiplying a Python list by 2 repeats the list twice.

NumPy array

import numpy as np

arr = np.array([10, 20, 30, 40])
print(arr * 2)

Output:

[20 40 60 80]

Multiplying a NumPy array by 2 multiplies each element by 2.

3. Creating a NumPy Array with np.array()

np.array() converts a Python list into a NumPy array.

marks = np.array([75, 80, 92, 65, 88])
print(marks)
print(type(marks))

Output:

[75 80 92 65 88]
<class 'numpy.ndarray'>

ndarray means N-dimensional array.

4. Creating Number Sequences with np.arange()

np.arange() creates a sequence of numbers.

Syntax

np.arange(start, stop, step)

start: starting value (included)

stop: stopping value (excluded)

step: difference between consecutive values

Example:

arr = np.arange(1, 11)
print(arr)

Output:

[ 1  2  3  4  5  6  7  8  9 10]

Example with a step of 2:

print(np.arange(2, 11, 2))

Output:

[ 2  4  6  8 10]

5. Equally Spaced Values with np.linspace()

np.linspace() generates a specified number of equally spaced values between two endpoints. Both endpoints are included by default.

Syntax

np.linspace(start, stop, number_of_values)

Example:

arr = np.linspace(0, 10, 5)
print(arr)

Output:

[ 0.   2.5  5.   7.5 10. ]

This creates 5 equally spaced values between 0 and 10.

Remember:

arange() is based on the step size.

linspace() is based on the number of values.

6. Creating Arrays of Zeros and Ones

np.zeros()

Creates an array filled with zeros.

print(np.zeros(4))

Output:

[0. 0. 0. 0.]

np.ones()

Creates an array filled with ones.

print(np.ones(4))

Output:

[1. 1. 1. 1.]

By default, these functions create arrays with floating-point values.

7. Using np.full() and np.eye()

np.full()

Creates an array of a specified size filled with the same value.

print(np.full(4, 7))

Output:

[7 7 7 7]

np.eye()

Creates an identity matrix: ones on the main diagonal and zeros elsewhere.

print(np.eye(3))

Output:

[[1. 0. 0.]
 [0. 1. 0.]
 [0. 0. 1.]]

8. NumPy Array Properties

Consider this array:

arr = np.array([10, 20, 30, 40, 50])

print("Shape:", arr.shape)
print("Dimension:", arr.ndim)
print("Size:", arr.size)
print("Data type:", arr.dtype)

Possible output:

Shape: (5,)
Dimension: 1
Size: 5
Data type: int64

The exact data type can vary depending on the system and how the array is created.

Property

Meaning

shape

Number of elements along each dimension

ndim

Number of dimensions

size

Total number of elements

dtype

Data type of the array elements

For a one-dimensional array containing 5 elements:

shape is (5,)

ndim is 1

size is 5

9. Two-Dimensional (2D) Arrays

A 2D array has rows and columns.

arr = np.array([
    [10, 20, 30],
    [40, 50, 60]
])

print(arr.shape)
print(arr.ndim)
print(arr.size)

Output:

(2, 3)
2
6

Explanation:

shape = (2, 3): 2 rows and 3 columns.

ndim = 2: the array has 2 dimensions.

size = 6: there are 6 elements in total.

10. Practice Questions

Try solving these questions yourself.

Create a NumPy array containing 5, 10, 15, 20, 25 and print it.

Create np.array([2, 4, 6, 8]). Multiply every element by 3 and print the result.

Use np.arange() to generate all even numbers from 2 to 20, including 20.

Use np.linspace() to generate 5 equally spaced values between 0 and 20, including both endpoints.

Create np.array([10, 20, 30, 40, 50, 60]) and print its shape, ndim, and size.

Create an array of 5 zeros.

Create an array of 4 ones.

Create an array of 3 elements, each equal to 9.

Create a 3 × 3 identity matrix using np.eye().

Create a 2D array with 2 rows and 3 columns, then print its shape, ndim, and size.

Quick Revision

np.array() → creates an array from a list or other input.

np.arange() → creates a sequence using a step size; the stop value is excluded.

np.linspace() → creates a specified number of equally spaced values.

np.zeros() → creates an array of zeros.

np.ones() → creates an array of ones.

np.full() → creates an array filled with a chosen value.

np.eye() → creates an identity matrix.

shape → dimensions in each direction.

ndim → number of dimensions.

size → total number of elements.

dtype → type of the elements.
