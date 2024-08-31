# `Wordle` Class Documentation

## Attributes

- **`alphabet_colors`** (`dict`):  
  Maps each letter of the alphabet to its current background color on the alphabet display. Initialized with all letters set to the default color.

- **`game_board`** (`list`):  
  A 2D list representing the game board. Each sublist corresponds to a guess attempt and contains dictionaries for each letter's display properties.

- **`input_box`** (`ipywidgets.Text`):  
  Widget for the user to input their guesses. Includes a placeholder and a descriptive label based on the selected language.

- **`language`** (`str`):  
  The current language code (e.g., `'en'` for English, `'de'` for German). Determines the language of messages and the word list URL.

- **`max_guesses`** (`int`):  
  The maximum number of allowed guesses in the game. Default is set to `6`.

- **`num_guess`** (`int`):  
  Tracks the current number of guesses made by the player.

- **`restart_button`** (`ipywidgets.Button`):  
  Button widget that allows the player to restart the game. Displays text based on the selected language.

- **`solution`** (`str`):  
  The word that the player needs to guess. It can be randomly selected from the word list or set by the user.

- **`submit_button`** (`ipywidgets.Button`):  
  Button widget for submitting guesses. Triggers the input handling process when clicked.

- **`words`** (`list`):  
  A list of valid 5-letter words fetched from the specified URL based on the selected language.

## Methods

- **`__init__(self, language='en', max_guesses=6)`**:  
  Initializes the `Wordle` game with default settings, including language selection and fetching the word list.

- **`end_game(self, success)`**:  
  Handles the end-of-game logic by displaying a success or failure message and disabling the submit button.

- **`fetch_words_from_url(self, url)`**:  
  Fetches words from the specified URL, decodes them, filters for 5-letter words, and stores them in the `words` list.

- **`get_user_solution(self, button)`**:  
  Presents an interface for the user to input their own solution word. Validates the input and sets it as the game's solution if valid.

- **`handle_input(self, _=None)`**:  
  Processes the user's guess from the input box. Validates the guess, updates the game board, and checks for win/loss conditions.

- **`print_alphabet(self)`**:  
  Generates and returns the HTML representation of the alphabet display with colored letters based on their current status.

- **`print_board(self)`**:  
  Generates and returns the HTML representation of the game board, displaying each guess with appropriate styling.

- **`restart_game(self, button)`**:  
  Restarts the game by reinitializing the `Wordle` instance with the current language setting.

- **`select_random(self, button)`**:  
  Selects a random word from the fetched word list as the solution and initiates the game interface.

- **`set_language(self, language_code)`**:  
  Sets the game's language, updates the word list URL accordingly, and fetches the new word list.

- **`set_user_solution(self, user_word)`**:  
  Validates and sets the user's input as the solution word if it exists in the word list and is 5 letters long.

- **`show_settings(self)`**:  
  Displays the settings screen, allowing the user to choose between a random word or entering a custom word, as well as selecting the language.

- **`start_game(self)`**:  
  Initializes the game state, including resetting guess counts, creating an empty game board, and setting up input widgets for guesses.

- **`update_board(self, guess)`**:  
  Updates the game board and alphabet colors based on the player's guess. Determines which letters are correct, present, or absent.

- **`update_display(self)`**:  
  Clears the current display and renders the updated game board, alphabet, input box, and control buttons.

## Additional Notes

- **Language Support**:  
  The `lang_dict` dictionary supports multiple languages. Currently, English (`'en'`) and German (`'de'`) are implemented. You can add more languages by extending this dictionary.

- **Color Schemes**:  
  The `colors` dictionary defines the color schemes for different states of the game, such as correct letters, wrong letters, and the default alphabet display.
