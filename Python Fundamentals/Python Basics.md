# Python Basics:
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
<colgroup span = "3"></colgroup>
<thead>
  <tr>
     <th colspan = "3" scope = "colgroup">Logical Operator Comparision</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Operator:</td>
    <td><a href = "https://github.com/BOLTZZ/Python">Python:</a></td>
    <td><a href = "https://github.com/BOLTZZ/Java">Java:</a></td>
  </tr>
  <tr>
    <td>NOT</td>
    <td>not</td>
    <td>!</td>
  </tr>
  <tr>
    <td>OR</td>
    <td>or</td>
    <td>||</td>
  </tr>
  <tr>
    <td>AND</td>
    <td>and</td>
    <td>&&</td>
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
