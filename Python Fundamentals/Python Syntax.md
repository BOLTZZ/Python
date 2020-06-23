# Syntax:
Lambda:
```python
function_name = lambda input : code #The code after the semicolon (:) gets returned.
multiply = lambda x,y : x * y
# Lambda is usefuls since you dont have write this out:
def multiply(self, x, y):
  return x * y
```
Loops:
```python
# While loop:
while i > 10 (condition):
  # execution
# For loop:
for i in range(0, 10) (condition):
  # execution
```
Statements:
```python
# If/else conditional statement:
if i <= 10 (condition):
  # execution
elif i > 100 (condition using else if):
  # execution
else (no condition for else):
  # execution
# One-line if/else conditonal statement:
if-true-return-this if boolean-conditon else if-false-return-this
# Try/Except statemnt to catch exceptions/errors:
try:
  int = int(input("Please enter a number:"))
except ValueError (type of error):
  print("Make sure to only enter a number. Nothing else!")
```
Lists:
* Lists usually store homogeneous items and are mutable. 
* The reverse function (list.reverse()) reverses a list object by swapping the 1st and last items, 2nd and 2nd to last items, and so on.
```python
cars = [] #Creates an empty list.
cars.append("Nissan", "Honda", "Buggati") #Adds items to the empty list.
num_of_cars = len(cars) #Gets the length of the list.
third_car = cars[2] #Gets the third car. Remember all lists/arrays start at 0.
#Theres a ton more you can do with lists and would be too much to write down here.
#Search the web :)
```
List Comprehension:
```python
numbers_from_10_to_60 = [i for i in range (10, 60)]
# The above is list comprehension since it uses a concise way to create a list.
# List comprehension is when you usually use one liner for loops or if/else loops to create a concise list.
# Without list comprehension:
numbers_from_10_to_60 = []
for i in range(10 60):
  numbers_from_10_to_60.append(i)
# List comprehension to sum the numbers (0 to 9) that are odd:
odds = sum([i for i in range(10) if i%2 == 1])
```
Dictionaries:
* Mappings of keys to items (key-value pairs) with keys being immutable and values being anything (lists, strings, and more). Dictionaries are mutable and can be used to perform fast lookups on unordered data. And, since dictionaries don't have any particular sequence, looping over dictionaries will be done arbitrily
```python
# Unlike lists, dictionaries contain keys and values:
people_ages = {"John":13, "Aaron":20, "Mary":28, "Naruto":34, "Kushina":50}
# Syntax: dictionary_name = {key:value}
# Accessing value(s):
john_age = people_ages["John"]
# Changing value(s):
people_ages["Aaron"] = 14
#Theres a ton more you can do with dictionaries and would be too much to write down here.
#Search the web :)
```
Dictionary Comprehension:
```python
# Dictionary comprehension is just like list comprehension:
list_60 = [i for i in range(10, 60)]
dict = {i:i/5 for i in list_60}
# This copies the values of the list_60 over to dict while dividing them by 2.
# Notice, the key for dict is the same value as list_60 but the value is the key divide by 2:
dict = {10:2.0, 11:2.2, 12: 2.4, 13: 2.6, 14: 2.8, and so on..}
```
Tuples:
* Tuples are immutable sequences with heterogeneous items.
* Many functions used by list objects can be used by tuple objects but, not the ones that change the items in the tuple (like .append()).
```python
contestant_names = ("Gerald", "Mikey", "Arnold", "Steven")
# Concatenate the previous tuple with a new tuple of names:
final_names = contestant_names + ("Derek", "Zabith", "Aaron", "Jenkin")
x = 12.3
y = 14.4
# Packing a tuple:
coordinate = (x, y)
# Unpacking a tuple into c1 and c2:
(c1, c2) = coordinate
# Creating a tuple with 1 value:
one_item = (2, )
```
Sets:
* Sets are unordered collections of disctinct hashable objects, hashable means sets can be used for immutable objects like strings or integers but not for mutable objects like lists or dictionaries. There are 2 types of sets, a <em>set</em> and a <em>frozen set</set>, a set is mutable while a frozen set is immutable.
* Sets don't have indicies and their elements are unique, not duplicated.
```python
# Created set using set() function:
example = set([1, 2, 3], 4)
len(example)
# The length of example is 4.
# Adds 5 but doesn't add 2 since 2 is already in set. NO DUPLICATE ITEMS:
example.add(5)
example.add(2)
males = set([1, 3, 4])
# Can use sets for mathematical operations:
females = example - males
# Set union (|):
everyone = males | females
# Intersection operation (&) which returns items in both sets:
everyone & set([1, 2, 3])
# Returns 1, 2, 3.
```
Set Comprehension:
* 
```python
```
Function:
```python
#Creating a function:
def function_name (self, other_inputs):
  #execution
  return statement
```
There are 4 basic types of actions in Python: 
 * Actions that don't take and no return
 * Actions that take some and no return
 * Actions that take some and return
 * Actions that take nothing and return
 
Though, in Python there is no predefined syntax for the datatype of the return object unlike Java.

Syntax for the 4 functions, in order:
```python
def function_name (self):
  # execution
def function_name (self, input):
  # execution
def function_name (self, input):
  # execution
  return foo
def function_name (self):
  # execution
  return foo
```
* Functions allow larger task to be divided into smaller tasks, something called *procedural decomposition*.
* All variables in a function are called *local variables* and only exist in that function, to use *global variables* used to global handle.
