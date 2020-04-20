# Syntax:
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
# Try/Except statemnt to catch exceptions/errors:
try:
  int = int(input("Please enter a number:"))
except ValueError (type of error):
  print("Make sure to only enter a number. Nothing else!")
```
Lists:
```python
cars = [] #Creates an empty list.
cars.append("Nissan", "Honda", "Buggati") #Adds items to the empty list.
num_of_cars = len(cars) #Gets the length of the list.
third_car = cars[2] #Gets the third car. Remember all lists/arrays start at 0.
#Theres a ton more you can do with lists and would be too much to write down here.
#Search the web :)
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
