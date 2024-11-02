# Advanced Dice Game 🎲

This is a web-based dice game that challenges players to score points by rolling combinations on five dice. With a maximum of six rounds and three rolls per round, the game incorporates strategic score selections and provides feedback on valid scoring options based on the roll outcomes.[TRY NOW](https://qyuzet.github.io/js-advance-dice-game/) 

## Table of Contents
- [Demo](#demo)
- [Features](#features)
- [Rules](#rules)
- [Score Combinations](#score-combinations)
- [How to Play](#how-to-play)
- [File Structure](#file-structure)
- [JavaScript Functionality](#javascript-functionality)

## Demo
You can try the game [here](https://qyuzet.github.io/js-advance-dice-game/).

## Features
- **Responsive Dice Roll Simulation**: Displays five dice that generate random values for each roll.
- **Score Selection**: Provides scoring options based on roll outcomes.
- **Round and Roll Management**: Tracks and limits rolls per round, progressing automatically after score selection.
- **Score History**: Shows a cumulative record of scores over six rounds.
- **Rules Toggle**: A button to show or hide game rules.

## Rules
1. The game has six rounds.
2. You can roll the dice up to three times per round.
3. Choose a score after each roll or roll again up to three times.
4. Selecting a score moves you to the next round; otherwise, you can roll again until your three rolls are used.

## Score Combinations
- **Three of a kind**: Sum of all five dice.
- **Four of a kind**: Sum of all five dice.
- **Full house**: Three of a kind and a pair - 25 points.
- **Small straight**: Four consecutive dice values - 30 points.
- **Large straight**: Five consecutive dice values - 40 points.

## How to Play
1. **Roll the Dice**: Click the "Roll the dice" button.
2. **Check Score Options**: Based on your roll, enabled score options will appear.
3. **Select a Score**: Choose an available scoring option to lock in your score for the round.
4. **Repeat for Six Rounds**: Play until you complete all six rounds, and view your total score in the score history.

## File Structure
- **index.html**: Contains the HTML structure and layout.
- **styles.css**: Provides styling for the game interface.
- **script.js**: Contains all game logic in JavaScript.

## JavaScript Functionality
Here's an overview of the key JavaScript code found in `script.js`:

### Variables and Selectors
- **`diceValuesArr`**: Array to store current dice values.
- **`score`, `round`, `rolls`**: Variables to keep track of the score, current round, and rolls.
- **DOM elements**: Cached references to the dice display, score options, and buttons.

### Core Functions

#### `rollDice()`
This function:
- Generates random values for each die (from 1 to 6).
- Updates each die's display to match the generated value.

#### `updateStats()`
This function:
- Updates displayed values for `rolls` and `round`.

#### `updateRadioOption(index, score)`
This function:
- Enables a score option based on the current roll.
- Updates the score shown in the option.

#### `getHighestDuplicates(diceValuesArr)`
This function:
- Analyzes the current dice values to determine possible scoring options.
- Enables the relevant scoring radio buttons based on the roll result.

#### `resetRadioOptions()`
This function:
- Resets all radio buttons, disabling them and clearing the score text.

#### Event Listeners
- **Roll Button (`rollDiceBtn`)**: Rolls the dice and updates the display. If the player has already rolled three times, it alerts the player to select a score.
- **Rules Button (`rulesBtn`)**: Toggles visibility of the game rules.
- **Keep Score Button (`keepScoreBtn`)**: Confirms the selected score, adds it to the total score, and moves to the next round.

## License
This project is open-source and available under the MIT License.
