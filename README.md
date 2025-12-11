# Python Hangman Game

This project is a fully functional implementation of the classic word game Hangman, written in Python. It features an interactive command-line interface, robust input validation, and a custom scoring algorithm.

## Project Overview

The goal of this project was to build a game engine that manages complex state transitions, handles user input edge cases, and manipulates strings dynamically based on game progress.

### Key Features Implemented

* **Dynamic String Manipulation**: The game tracks the user's progress in real-time, dynamically generating a display string (e.g., `*pp*e` for "apple") that reveals correct letters while keeping the rest hidden.

* **Complex Game Logic**:
    * **Variable Penalties**: The game distinguishes between vowels and consonants. Incorrect vowels penalize the player 2 guesses, while incorrect consonants cost only 1 guess.
    * **Input Validation**: The program sanitizes user input to handle case-insensitivity, prevents repeated guesses of the same letter, and rejects non-alphabetic characters without crashing.

* **"Help" Feature**: Implemented a logic gate allowing users to request a hint by typing `!`. The system identifies missing letters and reveals one at random, deducting 3 guesses as a trade-off.

* **State Management**: Tracks available letters, effectively removing them from the alphabet pool as they are guessed to guide the player.

* **Scoring Algorithm**: A custom scoring system calculates the player's performance based on word length, unique characters, and remaining guesses upon victory.

## Technical Concepts Applied

* **Data Structures**: Extensive use of **Lists** for mutable tracking of guessed letters and **Strings** for immutable word processing.

* **Control Flow**: Utilized `while` loops for the main game cycle and `if/else` logic trees to handle various guess outcomes (correct, incorrect, invalid, help request).

* **String Methods**: Applied methods like `.isalpha()` and `.lower()` for robust input handling.

## How to Play

1. Run the script from your terminal:
    ```bash
    python hangman.py
    ```
2. The computer will select a random word from `words.txt`.
3. You have **10 guesses** to identify the word.
4. Type `!` if you get stuck to use the "Help" feature (costs 3 guesses).

## Example Gameplay

```text
I am thinking of a word that is 4 letters long.
You have 10 guesses left.
Available letters: abcdefghijklmnopqrstuvwxyz
Please guess a letter: a
Good guess: *a**
