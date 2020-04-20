# How to Read and Edit Files on the Computer using Python:
3 types of files:
* Readable (reads the file).
* Writable (writes over the file and deletes the earlier text).
* Appendable (appends to the end of the file).
```python
path = "C:\\Users\\user\\PycharmProjects\\ACSLtest\\Test"
# This is the original path: "C:\Users\user\PycharmProjects\ACSLtest\Test"
# Then add one more backslash next to each existing slash so it looks like this:
# "C:\\Users\\user\\PycharmProjects\\ACSLtest\\Test"

with open(path, "r") as file_handle:
    text = file_handle.readlines()
    # Reads all the lines.
print(text, type(text))
# Prints out all the lines

with open(path, "r") as file_handle:
    text = file_handle.readline()
print(text)

with open(path, "r") as file_handle:
    text = file_handle.read(7)
    # Reads the file based on the number of characters specified in the parantheses.
    # AND PRINTS OUT THE ENTIRE WORD!!
    # Remember /n (newline) is considered a character so if 8 was in the parantheses nothing would be printed out.
    # But if 9 was in the parantheses 'T' would be printed out because its the 9th character.
print(text, type(text))

data_lst = ["jacob\n", "everyone\n", "oinkes\n"]

with open(path, "a") as file_handle:
# Make sure to have the "a" so its appendable and writelines so the text is added to the end of the file.
    text = file_handle.writelines(data_lst)
# This appends the data_lst to the end of the Test file.

with open(path, "w" ) as file_handle:
# Make sure to have the "w" so its writable.
    text = file_handle.write("Sup, m8\n")
    text = file_handle.write("AYY IM POPPING")
# Writes the string in the parantheses and replaces all earlier text.
# Check the Test file to see changes.
```
