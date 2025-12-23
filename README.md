# Guessing-Game
Guess the number thats it
import random
print("welcome to the number guessing game")

# it will generate a random number between 1 and 50, i have used random.randint because it will return the whole number between 1-50, like can return 27(int)number
secret_number=random.randint(1, 50)

# i have set the number of attempt
attempts=0
# i have used the while loop for run the guessing loop forever
while True:
    guess=input("guess a number between 1-50: ")

    if not guess.isdigit():
        print("please enter a valid number!")
        continue
# whenever python take input in return it gives string so i have put this int(guess) for return int result & attempts to monitor attempt gradually it will increase
    guess = int(guess)
    attempts +=1  
# plant some logic using if,elif,else and planted break if the number once correct it will break the code 
    if guess < secret_number:
        print("too low! Try again!")
    elif guess > secret_number:
        print("too high! try again!")
    else:
        print(f"correct! the number was {secret_number}.")
        print(f"you guessed it in {attempts}th attempts.")
        break
