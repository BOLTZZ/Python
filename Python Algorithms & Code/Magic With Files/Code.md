# Code:
* The code for each criteria is seperated by a space:
```python
path = "C:\\Users\\user\\PycharmProjects\\ACSLtest\\venv\\Homework Input"
# path is dependent on which file you want, make sure to add an extra slash to let the compiler know its a file root.

# Code for the 1st criteria:
num_of_lines = int(input("How many lines do you want the program to read? (starting from the beggening)"))
words = []
# Gathers input for the first criteria and sets up an empty array.
with open(path, "r") as file_handle:
    text = file_handle.readlines()
for i in range(0, num_of_lines):
    print(text[i])

# Code for the 2nd criteria:
numOfLines = int(input("How many lines do you want the program to read? (starting from the end)"))
start = len(text) - numOfLines
for i in range(start, len(text)):
    print(text[i])

# Code for the 3rd criteria:
with open(path, "r") as file_handle:
    words = file_handle.read().split()
largestLength = len(max(words, key=len))
largest_words = []
for i in range(0, len(words)):
    if largestLength == len(words[i]):
        largest_words.append(words[i])
if len(largest_words) == 1:
    print("The largest word is ", largest_words)
else:
    print("The largest words are ", largest_words)

# Code for the 4th criteria:
word = input("Type in a word to see its frequency of appearing in this file.")
frequency = words.count(word)
print("This word, ", word, ", appears ", frequency, " time(s).")

# Code for the 5th criteria (user dictionary):
user_dictionary = []
repeated_words = []
for i in range(0, len(words)):
    if words[i] in repeated_words:
        x = "2"
        #nothing
    else:
        user_dictionary.append(words[i])
        count = words.count(words[i])
        if count > 1:
            repeated_words.append(words[i])
        user_dictionary.append(count)
print("USER DICTIONARY:")
print("SYNTAX = WORD:NUMBER OF TIMES IT APPEARS")
smaller_word_list = []
for i in range(0, len(user_dictionary)):
    if ((i % 2) == 0):
        print(user_dictionary[i], ":", user_dictionary[i + 1])
        smaller_word_list.append(user_dictionary[i])

# Code for the 6th and 7th criteria:
count = []
for i in range(0, len(smaller_word_list)):
    num_of_vowels = 0
    num_of_vowels = num_of_vowels + smaller_word_list[i].count('a')
    num_of_vowels = num_of_vowels + smaller_word_list[i].count('A')
    num_of_vowels = num_of_vowels + smaller_word_list[i].count('e')
    num_of_vowels = num_of_vowels + smaller_word_list[i].count('E')
    num_of_vowels = num_of_vowels + smaller_word_list[i].count('i')
    num_of_vowels = num_of_vowels + smaller_word_list[i].count('I')
    num_of_vowels = num_of_vowels + smaller_word_list[i].count('o')
    num_of_vowels = num_of_vowels + smaller_word_list[i].count('O')
    num_of_vowels = num_of_vowels + smaller_word_list[i].count('u')
    num_of_vowels = num_of_vowels + smaller_word_list[i].count('U')
    count.append(num_of_vowels)
biggest_num = max(count)
smalles_num = min(count)
print("WORD(S) WITH THE MOST VOWELS:")
print("SYNTAX = WORD: NUMBER OF VOWELS")
for i in range(0, len(count)):
    if count[i] == biggest_num:
        print(smaller_word_list[i], " : ", count[i])
print("WORD(S) WITH THE LEAST VOWELS:")
print("SYNTAX = WORD: NUMBER OF VOWELS")
for i in range(0, len(count)):
    if count[i] == smalles_num:
        print(smaller_word_list[i], " : ", count[i])
```
