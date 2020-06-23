# Data Structures And Algorithms:
<strong>Data Structures:</strong>

Built-in Data Structures (click [here](https://github.com/BOLTZZ/Python/blob/master/Python%20Fundamentals/Python%20Syntax.md) for more information):
1. Lists - Lists are mutable array-like data structures that have each value as an item. They are defined by square brackets [value_1, value_2, ...].
2. Dictionaries - Dictionaries are mutable data structures, known as associative arrays or hashes, they contain keys and items with each key mapped to an item/value and are unordered key-value pairs. They are defined as {key_1 : value_1, key_2 : value_2, ...}.
3. Tuples - Tuples are the same as lists but, tuples are immutable unlike lists, and they're faster than lists. Also, tuples are represented by parantheses (value_1, value_2, ...).
4. Sets - Sets are immutable data structures that contain unordered, <em>unique</em> elements. They're commonly used for mathematical operations and can be defined as {unique_value, unique_value, ...}. 

User-Defined Data Structures:
1. Stack - Linear data structures based on the LIFO (Last In-First Out) principle. LIFO is kind of like a stack of plates, the last plate (top plate) is the first plate removed. It's built using the array structure and, in Python, the functions .push() and .pop() add and remove, respectivley. Stacks are usually used in recursive programming, reversing words, and more.
<img src = "https://media.geeksforgeeks.org/wp-content/cdn-uploads/gq/2013/03/stack.png" width = 300 height = 150>

2. Queue - Linear data structures based on FIFO (First In-First Out) principle. FIFO is kind of like a line to get into a place, the first person in line will get served first, not the last person in line. It's built using the array structure and, in Python, the functions .push() and .pop() add and remove, respectivley. Queues can be used for job scheduling management, traffic congestion management, and more.
  * *Enqueue* - Adding an item to the queue, if the queue is full, then it's an overflow condition.
  * *Dequeue* - Removing an item from the queue, the items are popped in the same order they're pushed. If the queue is empty then it's an underflow condition. 
  * *Front* - Getting front item of a queue.
  * *Rear* - Getting the last item of queue.
<img src = "https://media.geeksforgeeks.org/wp-content/cdn-uploads/gq/2014/02/Queue.png" width = 300 height = 150>

3. Binary Trees - Non-linear data structures with nodes and branches/egdes. The *root node* is from where the data originates, the node that precedes is the *parent node*, and the node below it/after is called the *child node*. The last nodes are called *leaves*, trees create a hierarchy which can be used in HTML pages, searching algorithms, and more.
<img src = "https://www.geeksforgeeks.org/wp-content/uploads/binary-tree-to-DLL.png" width = 300 height = 200>
4. Linked List - Linear data structures not stored consecutivley but linked to each other using pointers. The node of a linked list is data and a pointer called *next*, linked lists are usually used in image viewing applications, music player applications, and more.
<img src = "https://media.geeksforgeeks.org/wp-content/cdn-uploads/gq/2013/03/Linkedlist.png" width = 400 height = 150>

5. Graphs - Non-linear data structures with nodes (verticies) and edges, and the edges connect any 2 nodes in the graph. Graphs can be described as the most accurate representation of real word maps, they're used to find the shortest distance between nodes translating to the shortest distance between 2 real-word points (like home and work).
<img src = "https://www.geeksforgeeks.org/wp-content/uploads/undirectedgraph.png" width = 300 height = 150>

6. HashMaps - HashMaps are similar to dictionaries in Python. They can be used for phonebooks, populate data according to a list, and much more.

<strong>Algorithms:</strong>
* Algorithms are instructions/rules that're formulated in a finite, sequential order to solve problems, providing psuedocode for problems.

Writing Algorithms:
1. Figure out the exact problem.
2. Determine when you need to start.
3. Determine when you need to stop.
4. Formulate the intermediate steps.
5. Review the above steps.

Elements of A Good Algorithm:
* Steps should be finite, clear and understandable.
* Clear and precise description about inputs and outputs.
* Each step should have a defined output dependning only on the inputs of that step or preceding steps.
* The algorithm should be flexible and the steps should make use of general programming fundamentals.

Algorithm Classes:
1. Divide And Conquer - Divides the problem into sub-parts and solves each part seperatley.
2. Dynamic Programming - Divides the problem into sub-parts, remembers the parts and applies to similar ones.
3. Greedy Algorithms - Takes the easiest step in solving a problem without worrying about the complexity of future steps.

Tree Traversal Algorithms:
* Tree Traversal is visting each node in the tree exactly once to update or check them.

Three Types of Tree Traversal Algorithms:
1. In-order traversal is visiting the left nodes, root nodes, then right nodes.
<img src = "https://github.com/BOLTZZ/Python/blob/master/Extra%20Images%26Gifs/in-order.PNG" width = 150 height = 150>

2. Pre-order traversal is visiting the root nodes, left nodes, then right nodes.
<img src = "https://github.com/BOLTZZ/Python/blob/master/Extra%20Images%26Gifs/pre-order.PNG" width = 150 height = 150>

3. Post-order traversal is visiting left nodes, right nodes, then root nodes.
<img src = "https://github.com/BOLTZZ/Python/blob/master/Extra%20Images%26Gifs/post-order.PNG" width = 150 height = 150>

Sorting Algorithms:
1. Merge Sort - A stable sort that preserves the input order of equal elements in the sorted output. It works by dividing the unsorted list into n subsets, each subset containing 1 element (lists with only 1 element are considered to be sorted), then it repeatedly merges the sublists into new, sorted lists until there is only 1 sorted list remaining.
<img src = "https://www.w3resource.com/w3r_images/Merge-sort-example-300px.gif" width = 300 height = 150>

2. Bubble Sort - A comparision algorithm that first compares and sorts adjacent elements if they aren't in the specified order. It's repeated until the 1st element is in the correct place and this algorithm can take a long time for larger sets (worst time complexity). Thus, it's not very practical.
<img src = "https://upload.wikimedia.org/wikipedia/commons/0/06/Bubble-sort.gif" width = 300 height = 150>

3. Insertion Sort - Picks an item from the list and iterates until that item is in the place where it belongs. 
<img src = "https://upload.wikimedia.org/wikipedia/commons/9/9c/Insertion-sort-example.gif" width = 300 height = 150>

4. Selection Sort - Splits the list into 2 seperate lists with 1 list the sorted list and the other list the unsorted list. The sorted list is empty and all the elements are in the unsorted list then, the algorithm picks the smallest element from the unsorted list and moves it over to the sorted list. This is repeated until all the elements are in the sorted list, the selection sort is inefficent for large lists and insertion sort is generally better.
<img src = "https://i2.wp.com/algorithms.tutorialhorizon.com/files/2019/01/Selection-Sort-Gif.gif?ssl=1" width = 300 height = 150>

5. Shell Sort - It's kind of like a generalized version of insertion sort. It creates an interval/gap between elements and compares those 2 elements, swapping places based on difference, then by each iteration the gap becomes smaller and smaller until all the elements are sorted. The gap order based on length of the list (n) is n/2, then n/4, and so on.
<img src = "https://upload.wikimedia.org/wikipedia/commons/d/d8/Sorting_shellsort_anim.gif" width = 300 height = 150>

6. Quick Sort - Starts off by choosing a *pivot* which divides the list into 2 smaller subsets with 1 list containing elements smaller than pivot and the other containing elements larger than pivot. To avoid exponential run time the pivot can be random or the median of the first, middle, and last of the sub list. Starting from the 1st element we move up, if the element is smaller than pivot we continue but, if it's larger then we swap the elements. Now, we start from the other side and if the element is bigger than pivot we continue, if it's smaller we swap. NOTICE: The pivot value DOES NOT CHANGE. Time to recursivley sort the sub lists by repeating the sort for the sub lists until we're only left with 1 element in each sub list.
<img src = "https://upload.wikimedia.org/wikipedia/commons/9/9c/Quicksort-example.gif" width = 300 height = 150>

<strong>Searching Algorithms:</strong>
* Searching algorithms are used to search for some elements present in a dataset. There are many search algorithms such as Binary Search, Linear Search, Exponential Search, Interpolation.
1. Binary Search - Searchs for an element in a *SORTED* list by comparing the element with the element in the middle of the list, figuring out if the required element is smaller or larger, then splitting the list portion in half. This is done until the algorithm is found.
<img src = "https://d18l82el6cdm1i.cloudfront.net/uploads/bePceUMnSG-binary_search_gif.gif" width = 300 height = 150>

2. Linear Search - Searchs for an element by comparing it with each element in a list. Though, it's very time consuming.
<img src = "https://www.tutorialspoint.com/data_structures_algorithms/images/linear_search.gif" width = 300 height = 150>

3. Exponential Search - Works by finding a range where the element is present and performing a binary search, this means exponential search is meant for unbounded lists while binary search is meant for bounded lists. It's start of by creating sublists/subarrays of increasing size until the last element of a sublist/subarray is not greater than the specified element. Once the index of the sublist (i) is found then the specified element must be in between i/2 and i because the sublist size increases in the order of 1, 2, 4, 8 and so on.
<img src = "https://img.magiclen.org/albums/exponential-search/animation-541x141.gif" width = 300 height = 150>

4. Interpolation - Similar to binary search, interpolation performs the cutting in half of the list. But, unlike binary search, interpolation goes towards where the element may appear. For example, if the required element is closer to the last element then the search will start at the end of the side. The formula to find the theorized position of the element is based on this formula (uniformaly distributed array): position = low + (high - low) * (required_element - list[low])/list[high] - list[low]); low = starting index of the list and high = ending index of the list. The idea is to return a higher value of position when the element is closer to list[high] and lower when it's close to list[low].

<strong>Algorithm Analysis:</strong>
* Algorithm analysis can be performed before or after the implementation, priori (theoretical) or posterior (empirical) analysis, respectivley. 
1. Priori Analysis/Theoretical Analysis - The efficiency is measured by assuming all the factors are constant and don't affect the implementations. 
2. Posterior Analysis/Empirical Analysis - The efficiency is measured by gathering the actual values of time complexity, space complexity, execution time of the algorithm, and more.
