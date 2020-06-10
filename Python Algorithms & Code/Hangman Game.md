# Hangman Game:
* A python text based hangman game with only 1 letter guesses. A python (.py) file helps run the game and a text (.txt) file contains the words to choose from for the hangman game.

Code:
```python
# Import the required modules:
import random
import math
# Set an object (path) as the absolute path to the .txt file containing the words (wordlist)
# NOTE: The below path is an example path:
path = "C:\\Users\\user\\PycharmProjects\\hangman\\wordlist"
# Read in the lines of the file (each line contains only 1 word):
with open(path, "r") as file_handle:
    lines = file_handle.readlines()
# Generate a random number between 0 and 99 and find the corresponding line number and word:
word = lines[random.randint(0, 99)]
# Delete the "\n" at the end of the word:
word = list(word)
word.pop(len(word) - 1)
word = "".join(word)
# Tell the user what the game is:
print("A Game of Hangman:")
# Find the length of the word, set number of attempts, and max_attempts which will be sued later:
length = len(word)
attempts = math.floor(length * 1.5)
max_attempts = attempts
# Inform the user about the basics of the word and game:
print("Your word has", length, "letters. Also, you'll get a maximum of", attempts, "attempts.")
# Set a list (guesses) to empty as this will contain all the user's guesses so the user can't repeat guesses:
guesses = []
# Set copy to an empty string at it will contain "_ _ _" (the visual of the # of letters in the word). Also, it'll be updated as the user guesses correct letters:
copy = ""
# Fills up copy with the blank lines (_) corresponding to the number of letters:
for i in range(0, length):
    copy += "_ "
# Creates a loop that keeps on running as long the user has enough attempts left:
while attempts != 0:
    # Subtracts 1 attempt as the user uses an attempt:
    attempts -= 1
    # A loop that makes sure the user enters the correct format for a guess (1 letter):
    while True:
        # Asks the user for a letter:
        guess = input("Please guess a letter:")
        # Make sure it's a new guess (guess isn't in guesses) and the guess is a letter, then breaks the loop:
        if not(guess in guesses) and guess in "abcdefghijklmnopqrstuvwxyz":
            break
        # If the guess isn't a single letter or it's already been guessed, tells the user to guess properly:
        elif not(guess in "[a-z]"):
            print("Don't guess any special characters (like numbers)! And make sure it's only 1 letter!")
        elif guess in guesses:
            print("You already guessed that letter! Guess a new one.")
    # Adds the new guess to the existing list of guesses:
    guesses.append(guess)
    # Checks if the guess is a letter in the word:
    if guess in word:
        # Finds out which letters get found out and adds them to a string of the user's found out letters:
        for i in range(0, length):
            if guess == word[i]:
                list1 = list(copy)
                list1[i * 2] = guess
                copy = "".join(list1)
                bre = copy
        # Gets rid of the spaces in bre:
        bre = bre.replace(" ", "")
        # Checks if the user has fully guessed the word (bre = word):
        if bre == word:
            # Congratulates the user and checks if the user has maxed out his/her attempts or if there are more left:
            print("Congrats, you figured out the word:", word + ".")
            if attempts == 0:
                # Tells the user they used he/she maxed out the number of attempts (max_attempts):
                print("It took you the maximum amount of attempts ("+ str(max_attempts) +") to figure out the word.")
            else:
                # Tells the user how many attempts they took without maxing out:
                print("It took you", max_attempts - attempts, "attempts to figure out the word.")
            # Thanks the user and sets attempts = 0 so the loop will be broken:
            print("Thanks for playing!")
            attempts = 0
        # Checks if the user hasn't fully guessed the word and has some letters left:
        else:
            # Informs the user he/she guessed a letter in the word, shows them the current word, and tells them how many attempts are left:
            print("Your letter is in the word! Current word =", copy)
            print(attempts, "attempt(s) remaining.")
    # Checks if user guessed a letter incorrectly:
    else:
        if attempts != 0: # Checks if the user hasn't used up all the attempts.
            # Tells the user they guessed incorrectly and how attempts are left:
            print("Sadly, the letter you guessed isn't in the word. Current word =", copy)
            print(attempts, "attempt(s) remaining.")
        else: # Checks if the user has used up all the attempts.
            # Tells the user they guessed incorrectly, tells them the word, and thanks the user:
            print("Sadly, the letter you guessed isn't in the word and you've used up all your attempts. The word was:", word)
            print("Thanks for playing!")
```
Wordlist:
```python
jazz
discreet
slab
compliance
fate
curtain
census
calendar
anticipation
gesture
rhythm
random
season
deadly
innovation
impulse
seed
sin
complication
identification
paradox
rubbish
tissue
wear
wreck
bulb
stride
tire
motivation
proof
march
gloom
wrestle
reveal
test
chauvinist
fizz
digital
slice
awful
suspect
throat
fantasy
suite
lineage
snarl
stamp
selection
gown
chance
social
end
pot
breast
wriggle
grandmother
proportion
protect
prescription
awful
generate
command
censorship
stitch
start
interference
reaction
president
background
prejudice
laser
headquarters
trivial
cancer
literature
dull
vision
forget
brake
laborer
omission
banquet
trench
steak
promote
remedy
thigh
clash
pin
arch
slab
style
bacon
soak
palace
temporary
grimace
shoulder
mention
twin
```
In Action:

![1](https://github.com/BOLTZZ/Python/blob/master/Extra%20Images%26Gifs/hangman%20game.gif)
