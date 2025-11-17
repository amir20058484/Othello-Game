# Othello Game with AI (Minimax, AlphaBeta, Expectimax)

This is an implementation of the Othello (Reversi) board game with AI players using various decision-making algorithms such as Minimax, AlphaBeta Pruning, and Expectimax. The game allows a human player to compete against an AI player, or for two AI players to play against each other.

## Features

- **Human vs AI**: Play as Black or White against an AI.
- **Multiple AI Agents**: Choose from different AI algorithms to compete against:
  - **Random**: A basic random move AI.
  - **Greedy Flips**: AI that chooses the move with the most flips.
  - **Minimax**: Minimax decision-making with configurable depths (3, 4).
  - **Alpha-Beta**: Alpha-Beta Pruning for more efficient Minimax (depth 3-5).
  - **Expectimax**: AI that introduces randomness with a blunder rate, with depths 3 and 4.
  
- **Graphical Interface**: Built using `ipywidgets` to provide an interactive board and game controls.
- **Move Highlights**: Last AI move is highlighted, and possible moves for the human player are marked.
- **Pass and Restart**: The human player can pass their turn, and start a new game anytime.
- **Game Over Detection**: The game ends when there are no more valid moves for both players, and the winner is displayed.

## Installation

To run the game, you'll need to install `ipywidgets` and other dependencies. If you have Jupyter Notebook or JupyterLab, the following setup will get everything running:

1. **Install dependencies**:

    ```bash
    pip install ipywidgets
    ```

2. **Enable Jupyter widgets extension** (for Jupyter Notebook on Windows):

    ```bash
    jupyter nbextension enable --py widgetsnbextension --sys-prefix
    ```

## Running the Game

To run the game in a Jupyter Notebook:

1. Import the necessary modules and start the GUI:

    ```python
    from othello_gui import OthelloGUI
    gui = OthelloGUI()
    ```

2. The game interface will appear, allowing you to select an AI agent and choose your color (Black or White). The game will automatically update as you make moves and the AI takes its turns.

3. **AI Algorithms**:
    - **Minimax** and **Alpha-Beta** use tree search strategies to determine the best move based on a given depth.
    - **Expectimax** introduces a blunder rate (probabilistic errors) to make the game more challenging or unpredictable.

4. To start a new game, simply click "New Game" after the game is over.

## Game Rules

- **Board size**: 8x8 grid.
- **Objective**: The goal is to have more of your pieces on the board than your opponent at the end of the game.
- **Piece flipping**: A player can flip opponent's pieces if they make a move that sandwiches the opponent's pieces between their own.
- **Turn order**: The game alternates between the human player and the AI. The human player always starts with Black.

## AI Agents

### Minimax Agent
Minimax is a decision-making algorithm that explores all possible moves and chooses the one with the best outcome for the current player. The depth parameter controls how many moves ahead the AI will look.

### AlphaBeta Agent
AlphaBeta is an optimized version of Minimax. It prunes branches of the game tree that are not useful, improving performance.

### Expectimax Agent
Expectimax is used for decision-making when there's an element of randomness (like blunders). The agent considers not only the best outcome but also introduces errors based on a blunder rate.

## Example Gameplay

1. Choose an AI agent (e.g., `Alpha-Beta (depth=3)`) and start the game.
2. The human player will play first, and the AI will make its move after.
3. The game will update the board after each move, showing the current state of the game.

## Contributing

Feel free to fork the repository and make improvements or bug fixes! Here are some ideas for contributions:

- Improve AI strategies.
- Optimize performance for larger search depths.
- Add more AI algorithms.
- Improve the user interface.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
