# Pseudocode
## Initialization

1. Declare new variable "list_of_words"
2. Declare new variable word_to_guess and initialize it to a random word from  "list_of_words"
3. Declare new list variable "letters_to_guess"
4. Loop over word_to_guess to extract each letter and append it to "letters_to_guess"
5. Declare new variable "error_count" and initialize it to 0
6. Declare new list variable "letters_to_guess"
7. Declare new list variable "guessed_letters"
8. Declare new variable "hidden_word"
9. Loop over word_to_guess and remplace each letter by an  underscore and initialize "hidden_word" to that string
10. Declare new function "update_hidden_word" and initialize it to:
    1. declare new list variable "result"
    2. for every letter "i" in word_to_guess:
        1. if letter is in "guessed_letters" append "i" to "result" 
        2. else append "_" to "result"
    3. return a string made of joined letters of members in "result"
    
## Game

11. Print " Welcome to Hang(wo)man! Word to guess is: {"hidden_word"}. Please guess a letter:"
12. Input : User inputs a letter 
13. Check if input is a single letter
    1. If letter is not a single letter, prompt "Not a letter! 😭 Please try again!"
    2. Else, check if input is in "letters_to_guess"
        1. If yes : 
            2. add input to "guessed_letters"
            3. print "Congrats! 🥰 You found one letter."
            4. declare new variable "updated_hidden_word" and initialize it to the return value of "update_hidden_word"
            5. check if there is an underscore remaining in "updated_hidden_word"
                1. If yes, print the "The word to guess is {updated_hidden_word}"
                2. If not, print "You win!! 🎉"
        2. If not
            1. increment "error_count"
            2. check if "error_count" is above 9
                1. if yes, print "😵 You lost! Game over."
                2. else:
                    1. print "Oh no! This letter is not in the word we are looking for. You have {10 - "errors_count"} tries. 😬 Maybe try again?"
                    2. return to step 12
