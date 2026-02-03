import random

def number_guessing_game():
    # Pick a secret number (using randomizer)
    secret_number = random.randint(1, 100)
    # secret_number = 42  # you can hardcode if you prefer

    print("Welcome to the Number Guessing Game!")
    print("I've picked a secret number between 1 and 100. Try to guess it.")

    attempts = 0
    while True:
        try:
            # Get player's guess
            guess = int(input("Enter your guess: "))
            attempts += 1

            # Provide hints
            if guess < secret_number:
                print("Too Low!")
            elif guess > secret_number:
                print("Too High!")
            else:
                print(f"Congratulations! You guessed the secret number in {attempts} attempts.")
                break
        except ValueError:
            print("Please enter a valid number.")

# Run the game
number_guessing_game()
