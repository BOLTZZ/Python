# Lambda And Dictionary Comprehension:
What it does:
1. Lambda function which takes a, b, c as inputs and returns the largest elements.
2. Lambda function that takes in 2 arguments and returns the multiplcation. Only return a * b if a > b.
3. Using .sort() method, create a lambda function that sorts the list in ascending order. Refrain from using the reverse parameter.
4. Using sorted() and lambda sort the tuples in the list based on the 2nd last character of the 2nd item.
5. Given a dictionary, create a new dictionary with items where the 2nd value (not the key) is odd and less than 40.
Code:
```python
x = input("Please enter 3 numbers, seperated by spaces:")
x = [int(i) for i in x.split()]
a = x[0]
b = x[1]
c = x[2]
# Write a lambda function which takes a, b, c as inputs and returns the largest elements.
largest = lambda a, b, z: max(max(a, b), c)
print("The largest of", str(a) + ",", str(b) + ",", c, "is", largest(a, b, c))
# Write a lambda function that takes in 2 arguments and returns the multiplcation. Only return a * b if a > b.
multiply = lambda a, b: print(a, "*", b, "is", a * b) if (a > b) else print("The first factor must be larger than the 2nd factor.")
multiply(a, b)
# Using .sort() method, create a lambda function that sorts the list in ascending order. Refrain from using the reverse parameter.
list = [1.100, 2.10, 4.10000, 1.9, 1.29, 1.1999, 11.99]
print("Unsorted list =", list)
list.sort(key = lambda x: x) # I know that .sort() already sorts it into ascending order but I needed to use the lambda.
print(list, "has been sorted in ascending order!")
# Using sorted() and lambda sort the tuples in the list based on the 2nd last character of the 2nd item
lst=[ (19542209, "New York") ,(4887871, "Alabama"), (1420491, "Hawaii"), (626299, "Vermont"),(1805832, "West Virginia"), (39865590, "California")]
print("Unsorted list =", lst)
lst = sorted(lst, key = lambda x: x[1][-2])
print(lst, "has been sorted depending on the 2nd last character of the 2nd item.")
# Given a dictionary, create a new dictionary with items where the 2nd value (not the key) is odd and less than 40.
original_dict = {'jack': 38, 'michael': 48, 'guido': 57, 'john': 33}
print("Previous dictionary =", original_dict)
new_dict = {i:original_dict[i] for i in original_dict if original_dict[i] < 40 and original_dict[i]%2 != 0}
print(new_dict, "has been cropped down  depending of if the age of the person is odd and less than 40.")
```
See it in action:

![1](https://github.com/BOLTZZ/Python/blob/master/Python%20Algorithms%20%26%20Code/List%20Comprehension/lambda_dict.gif)
