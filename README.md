# Wordle Game (Python Implementation) [![Open All Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MHoffmannAC/wordle/blob/main/Wordle.ipynb)


## Project Overview

This Python project implements a versatile version of the classic Wordle game, featuring a user-friendly interface, multi-language support, and customizable settings. The game is designed to run in Jupyter notebooks or Google Colab environments, providing an interactive and engaging experience.

-----

## Features

- **Multi-Language Support**: The game supports both English and German, with the flexibility to add more languages. Each language has custom messages and labels, ensuring a tailored experience for users.

- **Customizable Word Selection**:
  - **Random Word**: Choose a random 5-letter word from a pre-defined list.
  - **User Input**: Allow users to enter their own 5-letter word as the solution.

- **Interactive UI**: The game provides a dynamic interface with:
  - An input box for guessing words.
  - A visual display of the game board and alphabet.
  - Colored feedback for correct, incorrect, and misplaced letters.

- **Adaptive Gameplay**: The game tracks and updates the state based on user input, providing feedback on each guess and managing game progress efficiently.

-----

## Coding Techniques

- **Object-Oriented Design**: The game logic is encapsulated in a `Wordle` class, which manages game state, user interactions, and UI updates. This approach organizes code and simplifies maintenance.

- **Dynamic Language and Word Handling**: The game uses dictionaries to handle language-specific messages and URL sources for word lists, enabling easy updates and additions.

- **Interactive Widgets**: Utilizes `ipywidgets` for creating interactive elements like text input, buttons, and visual displays, enhancing the user experience within a Jupyter notebook or Colab environment.

- **State Management**: Efficiently tracks game progress, including guesses, board updates, and game status, through a well-managed state system.

- **Visual Feedback**: Implements color-coded feedback for user guesses, providing clear visual cues for correct, incorrect, and partially correct letters.

-----

## Project Files

- [**Wordle.ipynb**](https://github.com/MHoffmannAC/wordle/blob/main/Wordle.ipynb): The main Jupyter notebook file containing the complete implementation of the game.
- [**wordle_class.md**](https://github.com/MHoffmannAC/wordle/blob/main/wordle_class.md): Brief overview of the wordle class summarizing its attributes and methods.
- **README.md**: This file, providing an overview of the project and instructions for use.

-----

## How to Play

1. **Start the Game**:
   - Open the notebook in Google Colab [![Open All Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MHoffmannAC/wordle/blob/main/Wordle.ipynb) or a Jupyter environment and run the cells to initialize the game.

2. **Choose Settings**:
   - Select the language and choose how to pick the solution word (random or user-defined).

3. **Play the Game**:
   - Enter your guesses in the provided input box and submit them using the submit button or by pressing Enter. The game will provide feedback on your guesses and update the board accordingly.

4. **End or Restart**:
   - Once the game ends, you can restart the game by clicking the restart button. The final screen will display whether you won or lost, along with the correct solution.

-----

## Installation and Setup

No additional installation is required if used in Google Colab. For other environments, ensure that `ipywidgets` and `IPython.display` are installed for interactive features.

The game has been tested using Python 3.10.12 in Google Colab.

-----

## Known Issues

- Submitting words via ENTER-key needs to be done with care. Too quick submission after typing in the word can cause wrongfully denial of the submitted word as it is not fully transmitted.
- The focus should be set on the input boxes to avoid having to click into the input-box with the mouse every time.
