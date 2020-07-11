# Libraries For Research:
<strong>Scope Rules:</strong>
* Each variable name belongs to a namespace and can be thought of as the context in which a given name exists. This is similar to how when you're talking with your friends about Dave, the context in the conversation let's them know which Dave you're talking about. Likewise, Python uses *scope rules* to figure out which variable x is being used and which function update is being used.
* Scope rules allow Python to search for the object, moving from the inner layers to the outer layers and uses the first x variable or update function it finds. The scope rule can be memorized by using the acronym, LEGB:
  1. L - Local (current function, function your in).
  2. E - Enclosing function (function that called the current function/local).
  3. G - Global (module in which the function was defined).
  4. B - Built-in (Python's built-in namespace).
* If Python can't resolve the name (find the object with the requested name) then it raises a name error exception, stopping the execution of the program.
* An example of LEGB:
```python
# This function tries to append the number 1 to an object/variable x:
def update():
  x.append(1)
# Running this function results in a name error since the name x isn't defined.

# Lets add some more code:
x = [2, 3]
update()
# Running the above portion modifies the list object x because Python finds an object called x in the global layer/scope using the LEGB rule.
# This shows that global variables can be modified. But, these types of functions that modify objects in a "behind the scenes" manner are said to have side effects and is a programming style that should be generally avoided because it can lead to programming errors.
```
<strong>NumPy module:</strong>
* NumPy is a Python module for scientific computation. One example of this is that NumPy array objects are n-dimensional arrays, being at the core for scientifict and numerical computations. Also, NumPy has tools to integrate the existing code with C, C++, and Fortran code. NumPy has many useful tools to perform linear algebra, generate random numbers, and much more. More information can be found on the [numpy.org](numpy.org) website.
* NumPy Arrays are another datatype, provided by NumPy, used to represent vectors or matricies. Unlike Python lists which can grow dynamically (you can change the size of the list) NumPy Arrays have a fixed size when they're constructed. Also, elements of the array have to be of the same datatype leading to more efficient and simpler code.
* We'll be making vectors and matricies using NumPy:
```python
import numpy as np
# A vector with 5 elements, containing only zeros as elements:
zero_vector = np.zeros(5)
# A matrix of 5 rows and 3 columns, containing only zeros as elements:
zero_matrix = np.matrix((5, 3))
# To create an empty array, np.empty can be used and the elements won't be initalized. But, this method should be used with care and generally shouldn't be used if your new to NumPy.
# Also, NumPy arrays can be created with specified values by using the np.array() function and the input is a list of numbers.
# Creating x and y vectors:
x = np.array([1, 2, 3])
y = np.array([2, 4, 6])
# Constructing a 2d array (matrix) can be done with a nested list object (2 by 2 matrix):
z = np.array([[1, 3], [5, 9]])
# Transposing a matrix (turning it sideways) can be accomplished via the tranpose method:
z.transpose()
```
* Indexing elements, regardless of dimensions (vectors or matricies), is pretty easy. For vectors (1d arrays) the index is just the desired position, keeping in mind that the indicies start at 0. With matricies (2d arrays) the 1st index specifies the row of the array and the 2nd index specifies the column of the array.
* Slicing arrays can be done, keeping in mind of the indexing logic, by entering the start and stop indicies (but Python will stop before the entered stop index). A colon (:) can be used to bring out either rows or columns. Also, indicies can be represented using other lists or NumPy arrays, this means that a boolean array can be used to represent the indicies too (like vector > 6, returns only elements greater than 6).
* One important note is that by slicing an array you get a view of the original object, so modifying the sliced array will modify the original array. This is different from indexing an array when what's returned to you is a copy of the array. This can be highlighted with an example:
```python

```
