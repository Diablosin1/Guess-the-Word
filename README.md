# Guess-the-Word
# Here's a simple code example of a "Guess the Word" game implemented in Python.

    import random

    # List of words for the game
    words = ["apple", "banana", "cherry", "grape", "orange"]

    # Select a random word from the list
    word = random.choice(words)

    # Create a list to store the guessed letters
    guessed_letters = []

    print("Welcome to Guess the Word Game!")
    print("Try to guess the word.")

    # Game loop
    while True:
        # Display the word with underscores for unguessed letters
        display_word = ""
        for letter in word:
            if letter in guessed_letters:
                display_word += letter
            else:
                display_word += "_"

    print("\n" + display_word)

    # Ask the player to guess a letter
    guess = input("Guess a letter: ").lower()

    # Add the guessed letter to the list
    guessed_letters.append(guess)

    # Check if the guessed letter is in the word
    if guess in word:
        print("Correct guess!")
    else:
        print("Wrong guess!")

    # Check if the player has guessed all the letters
    if all(letter in guessed_letters for letter in word):
        print("\nCongratulations! You guessed the word correctly!")
        break

    print("Thank you for playing!")
