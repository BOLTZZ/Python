# Python Regex:
[Python Regex Cheatsheet](https://www.rexegg.com/regex-quickstart.html)

What The Algorithm Does:
1. Finds all words starting with d or p.
2. Finds all numbers.
3. Finds strings that start with "The" and end with "Spain".

Code: 
```r
# Import re to use regex:
import re

# Find all words starting with d or p:
value = "abc 123 def 456 dot map pat"
pattern = "[dp]\w+"
print(re.findall(pattern, value))

# Find all numbers:
value = "Hello my Number is 123456789 and my friend's number is 987654321"
pattern = "\d+"
print(re.findall(pattern, value))

# Find if the string is starting with "The" and ending with "Spain".
value = "The rain in Spain"
pattern = "^The[\w\s\d]*Spain$"
print(re.findall(pattern, value))
```

In Action:
![1](https://github.com/BOLTZZ/Python/blob/master/Extra%20Images%26Gifs/regex.gif)
