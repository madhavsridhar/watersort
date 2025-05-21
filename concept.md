# Water Sort Game - Requirements Document

## Overview
Water Sort is a web-based puzzle game where the player sorts colored liquids in tubes so that each tube contains only one color or is empty. The game is implemented in a single HTML file with embedded CSS and JavaScript.

## Functional Requirements

### 1. Game Initialization
- The game starts with a splash screen where the player selects a difficulty (Easy, Medium, Hard).
- The player clicks the "Start game" button to begin.
- The game board is generated with a random number of tubes (between 8 and 14), with two tubes always empty.
- Each tube (except the empty ones) contains 4 units of colored liquid, distributed randomly but ensuring each color appears exactly 4 times.

### 2. Game Board
- Tubes are displayed in two rows, dynamically adjusting based on the number of tubes.
- Each tube is visually represented with colored segments for each unit of liquid.
- Tubes are clickable and highlight when selected.

### 3. Game Mechanics
- The player selects a tube to pour from, then selects another tube to pour into.
- Pouring is only allowed if:
  - The source tube is not empty.
  - The target tube is not full (max 4 units).
  - The top color of the source tube matches the top color of the target tube, or the target tube is empty.
  - The number of consecutive same-color units on top of the source tube fits in the target tube.
- Illegal moves are blocked with an alert.

### 4. Controls
- Undo: Reverts the last move.
- Reset: Restores the board to its initial state.
- Move counter: Displays the number of moves made.

### 5. Win Condition
- The game is won when all tubes are either empty or contain 4 units of the same color.
- On win, a message is displayed and the background color changes.

## Non-Functional Requirements
- Responsive design: The layout adapts to different screen sizes.
- Visual feedback: Selected tubes are highlighted, and win state is visually distinct.
- Accessibility: Uses semantic HTML and clear visual cues.

## Technical Details
- All logic is implemented in a single HTML file using vanilla JavaScript and CSS.
- No external dependencies except for Google Fonts.
- Game state is managed in a `WaterSortGame` class.
- The UI is dynamically rendered based on the game state.

## Future Enhancements (Suggestions)
- Add sound effects for moves and win state.
- Implement level progression or custom board sizes.
- Add a timer or scoring system.
- Save and load game state from local storage.
- Improve accessibility for keyboard and screen reader users.
