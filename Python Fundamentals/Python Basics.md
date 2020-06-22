# Python Basics:
* Python has 2 modes, *interative* and *standard* modes.
  1. Interactive mode - Meant for experimenting with code, one line or expression at a time. 
  2. Standard mode - Meant to run the programs from start to finish. 
* Python 3 is not backwards compatible with Python 2 which means that if a program is written in Python 3 it cannot be ran in Python 2.
* Python is an *interpreted* language which means the Python programs can be ran without first *linking* or *compiling* them.
* Python has objects with type, value, and identity. Type informs Python about the data type (string, int, list, and more), value is the value contained by the object, and identity is like an identity number for the object (each distinct object is stored in the computer's memory has its own identity number).
* Most objects have either functions, data, or both associated with them, known as *attributes*. The name of the attribute follows the name of the object, being seperated by a dot. The 2 types of attributes are either *data attributes* or *methods*. The data attribute is the value attached to an object while a method is a function attached to an object (performing some type of action on that object). Depending on the object type different methods may be avaliable. An *instance* is 1 occurrence of an object.
* A *Namespace* is a container of names shared by the objects that typically go together. 
* The ```dir(object_name)``` or ```dir(object_type)``` can return all the functions of an object.
* You can find out what a method does by using the help function: ```help(method_name)```.
* Python uses tabs to organize code so semicolons (;) are not required:
```python
def __init__(self, age, current_year): #Constructor method (Remember the self attribute).
  print("Hello World")
  year_born = current_year - age
  return year_born
  # The code up above is inside the Constructor becuase its tabbed.
current_year = 2020
age = int(input("What is your age?")) #This line does 3 things. Asks the user for his/her age, takes in the answer, and casts that answer from string to an int. 
year_born = init(age, current_year)#Calls the Constructor function and inputs in the required variables.
print("You were born in ", year_born)
#The code from lines 6 to 9 is not in the Constructor becuase its not tabbed.
```
* Logical operaters are the same as Java but unlike Java, they're written differently:
<table>
<colgroup span = "4"></colgroup>
<thead>
  <tr>
     <th colspan = "4" scope = "colgroup">Logical Operator Comparision</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Operator:</td>
    <td><a href = "https://github.com/BOLTZZ/Python">Python:</a></td>
    <td><a href = "https://github.com/BOLTZZ/Java">Java:</a></td>
    <td><a href = "https://github.com/BOLTZZ/R">R:</a></td>
  </tr>
  <tr>
    <td>NOT</td>
    <td>not</td>
    <td>!</td>
    <td>!</td>
  </tr>
  <tr>
    <td>OR</td>
    <td>or</td>
    <td>||</td>
    <td>|</td>
  </tr>
  <tr>
    <td>AND</td>
    <td>and</td>
    <td>&&</td>
    <td>&</td>
  </tr>
</tbody>
</table>
Though, the order of precedence is the same:

1. Parantheses
2. NOT
3. AND
4. OR
* A hastag (#) can be used to comment in Python.
* Datatypes are the same as Java:

1. Int = Whole Numbers (4).
2. String = Anything inside the qoutes ("..").
3. Double = Numbers with decimals (π).
4. Float = Numbers with decimals (Not accuarate as a double).
5. Boolean = True or false.
6. Char = A value that can be 16 bits in size (A).
* In operator:
```python
cars = ["Ford", "Lambo", "Ferrari"]
for car in cars: #The in operator helps iterate through each objects in the list, cars.
  print(car)
  #Prints each object
```
Lambda:
* The lambda creates a simpe function that may take in input(s) and return something. This is all done on one line. 
* Lambda always returns whatever is after the semicolon (:).
```python
add = lambda x, y : x + y
# The above is a simple add function
```
