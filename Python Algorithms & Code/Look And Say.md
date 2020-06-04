# Look And Say Sequence:
Explained:

A brief summary of a look and say sequence is an algorithm that prints out the number of times a digit appears and then the number. For example, 12 would be 1112 since the digits of 12 (1 and 2) only appear once, each. Another example is, 133154211 would be 11231115141221. For more detailed information visit this Wikipedia [page](https://en.wikipedia.org/wiki/Look-and-say_sequence).

Code:
```r
# Asks user for a number:
input = input("Please enter number:")
# Converts each digit in the string into a list of each digit:
num = [d for d in str(input)]
# Creates an empty list that will have each item as number of times a digit appears and the digit:
divided = []
# The function that fills up divided with number of times the digit appears and the digit as 1 item:
def create_count_and_digit(temp, divided):
    # Sets k to 1 and last to the first item of temp:
    k, last = 1, temp[0]
    # Checks if the length of the user's number (temp) is 1 and then just adds k and last to divided (concatenated):
    if len(temp) == 1:
        count_digit = str(k) + str(last)
        divided.append(count_digit)
    # Loop from the 2nd item of temp to the length of temp:
    for i in range(1, len(temp)):
        # Checks if the ith entry of temp is equal to last, then adds 1 to k:
        if temp[i] == last:
            k = k + 1
            # Checks if the ith entry of temp is the last entry of temp and sets count_digit to k and last (concatenated), adding count_digit to divided:
            if i == len(temp) - 1:
                count_digit = str(k) + str(last)
                divided.append(count_digit)
        # Does this if the ith entry of temp isn't equal to last:
        else:
            # Sets count_digit to k and last (concatenated), adding count_digit to divided. Also k = 1:
            count_digit = str(k) + str(last)
            divided.append(count_digit)
            last = temp[i]
            k = 1
            # Checks if the ith entry is the last entry in temp:
            if i == len(temp) - 1:
                # Sets count_digit to k and last (concatenated), adding count_digit to divided:
                count_digit = str(k) + str(last)
                divided.append(count_digit)
    # Returns divided:
    return divided
# Sets a variable (look_say) to all the entries of divided (based on num) joined together with no whitespace:
look_say = "".join(create_count_and_digit(num, divided))
print(look_say)
```
In Action:

![1](https://github.com/BOLTZZ/Python/blob/master/Extra%20Images%26Gifs/look%20and%20say.gif)
