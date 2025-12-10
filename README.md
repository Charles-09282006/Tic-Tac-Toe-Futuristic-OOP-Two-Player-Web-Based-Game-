# Tic-Tac-Toe (Futuristic OOP Two-Player Web-Based Game)

## Project Overview

## Game Objectives
- Place your mark/symbol (X or O) to get three cells/boxes in a row (vertical, horizontal, or diagonal).
- Strategically anticipate your opponent's moves at your chosen difficulty (Very Easy, Easy, Medium, Hard, or Very Hard).

## Win/Lose Conditions
- **Win:** You (your mark/symbol) complete any of the 8 winning lines.
- **Lose:** Your opponent completes a line first.
- **Draw:** All 9 cells/boxes are filled with no winning line.
  
## Technology Stack
- **Backend:** PHP 8.1 or higher
- **Frontend:** HTML5, CSS3, JavaScript (ES6)
- **Assets:** Animated GIF Background and Looping Background Music

## How to Play
1. **Launch the Game:**
   - Open "index.php" in your browser (Google Chrome or Microsoft Edge) via a local PHP Server (NOTE: Your PHP Server must be at version 8.1 or higher in order for the game to work perfectly).
2. **Choose your Mode:**
   - **Player vs Player (PvP):**
       - Both players take turn on placing X and O by clicking a cell with a mouse or using a keyboard.
   - **Player vs CPU (PvC):**
       - You play as X, while the CPU play as O. Choose a difficulty (Very Easy, Easy, Medium, Hard, Very Hard) on the main menu. CPU responds after your turn.

3. **Controls:**
   - **Mouse:** Select a cell/box to place your mark/symbol.
   - **Keyboard:**
       - **Up Arrow Key:** Move Up
       - **Down Arrow Key:** Move Down
       - **Left Arrow Key:** Move to the Left
       - **Right Arrow Key:** Move to the Right
       - **Enter/Space:** Place your mark/symbol
         
4. **HUD Options:**
   - **Toggle Music:** Players can turn the background music on/off.
   - **Try Again:** When the player wins/loses the game, it will restart the current match instantly.
   - **Return to Main Menu:** Goes back to the main menu (index.php)
     
5. **Game Flow:**
   - The HUD (Head-Up Display) shows whose turn it is.
   - Each move is recorded in the "Move History" section.
   - When the game ends, a "Win/Lose/Draw" Screen appears with options to restart or return to the main menu.

## Prerequisites
- Visual Studio Code
    - **Extensions:**
        - HTML/CSS Support (by ecmel)
        - IntelliSense for Css class names in HTML (by Zignd)
        - StandardJS - JavaScript Standard Style (by Standard)
        - PHP Intelephense (by Intelephense)
        - PHP Server (by brapifra)
        - Live Server (by Ritwick Dey)
- PHP 7.4+ (or higher) installed locally, or a web server that is capable of running PHP.
- A modern browser (Google Chrome or Microsoft Edge)
    - **Extensions:**
        - Live Server Web Extensions

## OOP Implementations
- **Encapsulation:**
    - Private properties in 'BaseConfig', 'CpuPlayer', and 'Board' keep internal state safe. Accessed via getters/setters (e.g., 'isMusicEnabled()', 'getCells()').
- **Inheritance:**
    - 'HumanPlayer' and 'CpuPlayer' extend the 'Player' base class; 'GameConfig' extends 'BaseConfig'.
- **Abstraction:**
    - Abstract classes/methods define contracts:
        - 'Player' declares 'getType()' for polymorphic behavior.
        - 'BaseConfig::validate()' requires concrete validation logic.
- **Polymorphism:**
    - 'HumanPlayer' and 'CpuPlayer' implement 'getType()' differently. 'Game' accepts any 'Player' subtype, enabling mode flexibility without changing the game's aggregation logic.

## Video Demonstrations
- **Charles Cristian Salting:**
    - 
- **Chezko Jomrey Tupas:**
    - 
- **Marc Anthony Bunan:**
    - [Watch Video](https://drive.google.com/drive/folders/1yyKCgETnc50FgppQ3CqSQtz5XJ3jgPOk?usp=sharing)
- **Alorich Dayrit:**
    - 

## Notes to Remember
- CPU Difficulty Levels:
    - **Very Easy:** Random
    - **Easy:** Random with occasional blocking
    - **Medium:** Heuristic (Win/Block/Center/Corners)
    - **Hard:** Minimax (limited depth)
    - **Very Hard:** Minimax (deep/full search)
- Each PHP Classes initialize and validate the game configuration player/board models. The interactive loop and AI run in JavaScript for responsiveness.
