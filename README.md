# TicTacToe

This program is a Unity implementation of the Tic Tac Toe game where the opponent is an artificial intelligence (AI) with two difficulty levels: easy and hard. "Easy" uses a random move among the available ones and an optimal selection using the minimax algorithm with a 50% chance of being one or the other, while "hard" only uses the optimal selection with the minimax algorithm.

### Functionalities

The main class is `TicTacToeAI`, which manages most of the game logic, maintaining the board state and determining win or loss conditions. The game starts when the board and game state are initialized. The `PlayerSelects` method is called when the user clicks on a cell, and `AiSelects` determines the move that the AI will make.

#### ClickTrigger

The `ClickTrigger` class handles user interactions with the game cells. Each cell has a `ClickTrigger` component that detects clicks and communicates with `TicTacToeAI`. Upon initialization, this class subscribes to the `onGameStarted` event, allowing all cells to be clickable. Then, when the user clicks on a cell, `OnMouseDown` calls `PlayerSelects` from `TicTacToeAI`, passing the cell coordinates.

#### Other Classes

- **EndMessage**: Displays the game result.
- **GamePiece**: Manages board animations.
- **RetryButton**: Provides the functionality to retry the game.
