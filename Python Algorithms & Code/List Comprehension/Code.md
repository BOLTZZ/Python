Here is the code:
```python
def main():
    #Asking for a number between 1 and 9.
    while True:
        user_number = int(input("Please enter a number between 1 and 9:"))
        if 1 <= user_number <= 9:
            break

    # Create a list of numbers from 1 to 1,000 that are divisble by the user's number.
    divisible_user = []
    for i in range(1, 1000):
        if i % user_number == 0:
            divisible_user.append(i)
    print("Numbers from 1 to 1,000 that are divisible by", user_number)
    print(divisible_user)

    # Create a list of numbers from 1 to 1,000 that have a digit of the user's number in the number.
    contains_user = []
    for i in range(1, 1000):
        str_i = str(i)
        if str_i.count(str(user_number)) > 0:
            contains_user.append(i)
    print("Numbers from 1 to 1,000 that have a digit of", user_number, "in the number")
    print(contains_user)

    # Count the number of spaces in a string.
    user_input = input("Please enter a string:")
    num_of_spaces = user_input.count(" ")
    print("Your string has", num_of_spaces, "spaces.")

    # Create a list and remove all the vowels in a string.
    user_input = input("Please input a new string:")
    user_list = list(user_input)
    num_to_remove = []
    vowels = ['a', 'A', 'e', 'E', 'i', 'I', 'o', 'O', 'u', 'U']
    for i in range(0, len(user_list)):
        if user_list[i] in vowels:
            num_to_remove.append(i)
    for i in range(0, len(num_to_remove)):
        remove_number = num_to_remove[i] - i
        user_list.pop(remove_number)
    print("New string with removed vowels =", '' .join(user_list))

    # Create a list of words that are less than or equal to the user's number of letters.
    user_input = input("Please input a list, separate each item of the list by whitespace:")
    four_letter_words = []
    word_list = user_input.split()
    for i in range(0, len(word_list)):
        if len(word_list[i]) <= user_number:
            four_letter_words.append(word_list[i])
    print("The items with", user_number, "or less letters in your inputted list are: ", four_letter_words)

# The following to run the program:
if __name__ == "__main__":
    main()
```



```python
def main():
    # Create a list of numbers from 1 to 1,000 that are divisble by 7.
    divisible_7 = []
    for i in range(1, 1000):
        if i % 7 == 0:
            divisible_7.append(i)
    print(divisible_7)

    # Create a list of numbers from 1 to 1,000 that have a digit 2 in the number.
    contains_2 = []
    for i in range(1, 1000):
        str_i = str(i)
        if str_i.count("2") > 0:
            contains_2.append(i)
    print(contains_2)

    # Count the number of spaces in a string.
    user_input = input("Please enter a string:")
    num_of_spaces = user_input.count(" ")
    print("Your string has", num_of_spaces, "spaces.")

    # Create a list and remove all the vowels in a string.
    user_input = input("Please input a new string:")
    user_list = list(user_input)
    num_to_remove = []
    vowels = ['a', 'A', 'e', 'E', 'i', 'I', 'o', 'O', 'u', 'U']
    for i in range(0, len(user_list)):
        if user_list[i] in vowels:
            num_to_remove.append(i)
    for i in range(0, len(num_to_remove)):
        remove_number = num_to_remove[i] - i
        user_list.pop(remove_number)
    print("New word with removed vowels =",'' .join(user_list))

    # Create a list of words that are less than or equal to 4 letters.
    user_input = input("Please input a list, separate each item of the list by whitespace:")
    four_letter_words = []
    word_list = user_input.split()
    for i in range(0, len(word_list)):
        if len(word_list[i]) <= 4:
            four_letter_words.append(word_list[i])
    print("The items with four or less letters in your inputted list are: ", four_letter_words)


if __name__ == "__main__":
    main()
```
