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
