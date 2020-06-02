# Map Function:
* The map function (map(function, iterable)) applies a certain function to each item in an iterable (like a list).
What the program does:
1. Squares each number in a list.
2. Doubles each number in a list.
3. Reverses each word in a list.
4. Finds which ages qualify for discounts.
5. Finds the positive digits in a string of letters and numbers (doesn't use the map function).

Code:
```r
# Asks user to enter numbers, seperated by whitespace, and squares each of the user's numbers:
list1 = input("Please enter numbers, seperated by spaces:").split()
list1 = [int(d) for d in list1]
print("Your numbers =", list1)
squared = list(map(lambda x: x*x, list1))
print("Squared numbers =", squared)

# Returns the double of user's numbers:
mulitplied = list(map(lambda x: 2*x, list1))
print("Double of the numbers =", mulitplied)

# Asks user to enter words, seperated by whitespace, and reverses each word:
listOfStr = input("Please enter words or letters, seperated by whitespace:").split()
print("Your words =", listOfStr)
reverse = list(map(lambda x: x[::-1], listOfStr)) # Uses slicing to reverse the string.
print("Reversed words =", reverse)

# Asks for family member ages and finds which ages qualify for discounts:
ages = input("Please enter your family member ages, seperated by whitespaces:").split()
ages = list(map(lambda x: x if int(x) >= 62 or int(x) <= 5 else "", ages))
print("Ages that qualify for discounts =", ", ".join(list(filter(lambda x: x != "", ages))))

# Asks user for an input of a mix of digits and letters and filters out the letters to only obtain the positive digits:
string_input = input("Please enter something, a mix of digits and letters:")
only_digits = list(filter(lambda x: x if x.isdigit() else "", string_input)) # isdigit() only finds posiive digits.
print("Only positive digits from input =", only_digits)
```
In Action:

![1](https://github.com/BOLTZZ/Python/blob/master/Extra%20Images%26Gifs/map_example.gif)
