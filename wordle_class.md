# `Wordle` Class Overview

## Attributes

- **`alphabet_colors`**: `dict` - Dictionary with background colors for each letter.
- **`game_board`**: `list` - 2D list representing the game board.
- **`input_box`**: `ipywidgets.Text` - Input box widget for entering guesses.
- **`language`**: `str` - Currently selected language code.
- **`max_guesses`**: `int` - Maximum number of allowed guesses.
- **`num_guess`**: `int` - Current number of guesses made.
- **`restart_button`**: `ipywidgets.Button` - Button widget to restart the game.
- **`solution`**: `str` - The word to be guessed.
- **`submit_button`**: `ipywidgets.Button` - Button widget to submit guesses.
- **`url`**: `str` - URL for fetching valid words.
- **`words`**: `list` - List of valid words fetched from the URL.

## Methods

- **`fetch_words_from_url()`**: Fetches words from the specified URL and filters them to include only 5-letter words.
- **`get_user_solution(button)`**: Allows the user to input their own solution word and validates it.
- **`handle_input(button)`**: Processes the player's guess, updates the game state, and provides feedback.
- **`handle_input_from_submit(text)`**: Handles the Enter key press in the input box by calling the `handle_input()` method.
- **`print_alphabet()`**: Generates the HTML representation of the alphabet display with colored letters.
- **`print_board()`**: Generates the HTML representation of the game board with styled cells.
- **`restart_game(button)`**: Restarts the game by reinitializing the `Wordle` instance.
- **`select_random(button)`**: Selects a random word from the fetched word list as the solution and starts the game.
- **`set_language(language_code)`**: Sets the word list URL based on the selected language and proceeds to word selection.
- **`set_user_solution(user_word)`**: Sets the user's input as the solution if it is valid and starts the game.
- **`show_settings()`**: Displays the settings screen with buttons for word or language selection.
- **`start_game()`**: Initializes the game state and sets up the game interface.
- **`update_board(guess)`**: Updates the game board and alphabet colors based on the player's guess.
- **`update_display()`**: Clears the current display and renders the updated game board, alphabet, and input widgets.
