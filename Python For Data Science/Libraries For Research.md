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
z1 = np.array([1,3,5,7,9])
# Slice 1,3, and 5 from z1 to w:
w = z1[0:3]
w[0] = 3
# The contents of w are [3, 3, 5] with the contents of z1 being [3, 3, 5, 7, 9]. This shows that modifying a spliced array modifies the original array.
# Now, let's use indexing
ind = np.array([0, 1, 2])
w = z1[ind]
# Another way is: w = z1[0, 1, 2]
w[0] = 3
# The contents of w are [3, 3, 5] with the contents of z1 being [1, 3, 5, 7, 9]. This shows that modifying an indexed array doesn't modify the original array since copies are returned.
```
* NumPy provides a way to construct arrays with start and end values and an uniform space between elements. We can create an array starting with 0, ending with 100, and having 10 uniformly space elements via NumPy linspace function:
```python
np.linspace(0, 100, 10)
# For 10 logarithmically spaced elements we can use the logspace function. The syntax for the logspace function is: np.logspace(log_of_starting_point, log_of_ending_point, number_of_elements)
np.logspace(np.log10(250), np.log10(500), 10) #This array starts at 250, ends at 500, and has 10 elements.
# The shape attribute can be called to find the shape of an array and size function for size. The parantheses aren't used since shape and size aren't functions, they're data attributes:
x = np.array([1, 2, 3], [4, 5, 6])
x.shape # Returns (2, 3), 2 rows by 3 columns.
x.size # Returns 6 for 6 elements.
# We can create a vector of 10 random elements (via NumPy's random module function), see if any of the elements are greater than 0.9 (any function), and see if all the elements are greater than or equal to 0.1:
y = np.random.random(10) # Creates 10 random elements from 0 to 1
np.any(y > 0.9) 
np.all(y >= 0.1)
```
<strong>Matplotlib and Pyplot:</strong>
* Matplotlib is a Python plotting library that produces publication-quality figures, it can be used in both Python scripts and Python interactive mode. Pyplot is a collection of functions useful for interactive mode for when you need to explore a dataset or visually examine the simulation results. Plyplot provides what is sometimes called a state machine interface to the matplotlib library. It can be loosely thought of a process where figures are create one at a time and all commands affect the current figure/plot. 
```python
# Import matplotlib.pyplot as plt:
import matplotlib.pyplot as plt
# We can use the plot function which, when given 1 argument, plots the elements in the list as y values with x values starting at 0 and incrementing by 1 for each element:
plt.plot([0,1,4,9,16]) # The 1st argument specifices the x coordinates, the 2nd argument specifies the y coordinates, and the 3rd argument is a format string which specifies color, marker, and line type.
# Plotting x and y coordinates with design elements defined:
x = np.linspace(0, 10, 20)
y1 = x**2.0 #x coordinates squared.
y2 = x**1.5
plt.plot(x, y1, "bo-", linewidth = 2, markersize = 4) #This plots the x and y1 coordinates with a formated string which represents using a blue line, circle points, and a solid line (b = blue, o = circle, - = solid). Also, the line width is set to 2 and marker size is set to 4.
plt.plot(x, y2, "gs-", linewidth = 2, markersize = 4) #Green, solid line with square points.
```
* Adding legends (legend() function), adjusting axes (axis() function), setting axis labels (xlabel() and ylabel() functions), and saving figures (savefig() function) can help customize plots:
```python
x = np.linspace(0, 10, 20)
y1 = x**2.0 
y2 = x**1.5
plt.plot(x, y1, "bo-", linewidth = 2, markersize = 4, label = "First")
plt.plot(x, y2, "gs-", linewidth = 2, markersize = 4, label = "Second")
# Labeling the axes, the label names accept LaTeX:
plt.xlabel("X")
plt.ylabel("Y")
# Resizes the axes to fit the graph:
plt.axis([-0.5, 10.5, -5, 105]) #plt.axis([xmin, xmax, ymin, ymax])
# Creates a legend using the predefined label keyword arguments:
plt.legend(loc = "upper left") 
# Save the plot file as a pdf:
plt.savefig("myplot.pdf")
```
Graph:

<img src = "https://github.com/BOLTZZ/Python/blob/master/Extra%20Images%26Gifs/plot.PNG" width = 300 height = 200>

* Sometimes it's useful to have 1 or more axes to be logarithmic which means that axis/axes need(s) to be transformed using a log function. The base defaults to 10 but can be changed. Some functions to help with logarithmic transformations are semilogx() which plots x-coordinates on a log scale and y-coordinates in the original scale, semilogy() which plots the x-coordinates in the original scale and the y-coordinates on a log scale, and loglog() plots both x and y coordinates on a log scale.
* To help illustrate the usefulness of logarithmic plots we can consider a function of the form: y = x<sup>α</sup>, depending on the value of α (alpha) the function can be linear, quadratic, and more. The log of the function can be taken, resulting in: log(y) = α * log(x), setting log(y) = y' and log(x) = x' results in: y' = α * x'. This means the graph is now a straight line with α defining the slope. 
* An example of a loglog() plot using the previous example:
```python
x = np.linspace(0, 10, 20)
y1 = x**2.0 
y2 = x**1.5
plt.loglog(x, y1, "bo-", linewidth = 2, markersize = 4, label = "First")
plt.loglog(x, y2, "gs-", linewidth = 2, markersize = 4, label = "Second")
# Labeling the axes, the label names accept LaTeX:
plt.xlabel("X")
plt.ylabel("Y")
# Resizes the axes to fit the graph:
plt.axis([-0.5, 10.5, -5, 105]) #plt.axis([xmin, xmax, ymin, ymax])
# Creates a legend using the predefined label keyword arguments:
plt.legend(loc = "upper left") 
# Save the plot file as a pdf:
plt.savefig("myplot.pdf")
```
Graph (Note: logspace() can be used to get evenly spaced x points):

<img src = "https://github.com/BOLTZZ/Python/blob/master/Extra%20Images%26Gifs/loglog.PNG" width = 300 height = 200>

* Histograms can be generated using the hist() function from the plt library:
```python
import matplotlib.pyplot as plt
import numpy as np
#We can generate 1,000 samples/draws from a standard normal distribution using the np.random.normal() function:
x = np.random.normal(size = 1000)
# Create histogram:
plt.hist(x)
```
Graph:

<img src = "" width = 300 height = 200>

* We can add more features to the histogram:
```python
# Normalize histogram (on the y-axis provide proportion of observations falling in corresponding x coordinate) and set the bin widths:
plt.hist(x, normed = True, bins = np.linspace(-5, 5, 21))
```
