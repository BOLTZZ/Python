# Data Structures And Algorithms:
<strong>Data Structures:</strong>

Built-in Data Structures:
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
1. In-order traversal is visiting the left nodes, root node, then right nodes.

2. 
