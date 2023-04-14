# Pseudocode
## Initialization

- Declare new variable list_of_words
- Declare new variable word_to_guess and initialize it to a random word from  list_of_words
- Declare new list variable letters_to_guess
- Loop over word_to_guess to extract each letter and append it to letters_to_guess
- Declare new variable error_count and initialize it to 0
- Declare new list variable letters_to_guess
- Declare new list variable guessed_letters
- Declare new variable hidden_word
- Loop over word_to_guess and remplace each letter by an underscore and initialize hidden_word to that string

## Game

- Prompt " Welcome to Hang(wo)man! Word to guess is: {hidden_word}. Please guess a letter:"
- User inputs a letter 
- Check if input is a single letter
    - If letter is not a single letter, prompt "Not a letter! Please try again!"
    - If input is a single letter, check if input is in letters_to_guess
        - If yes : add input to guessed_letters

## End 

